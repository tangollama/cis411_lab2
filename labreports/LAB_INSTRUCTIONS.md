# CIS 411 Lab 2: GitHub + Docker + CircleCI + Heroku
The purpose of this lab is to get hands on experience working with Docker, CircleCI, and a Cloud Service Provider like Heroku to create a CI/CD pipeline. Though the lab is generally paint by numbers, the hands on experience with the tools is meant to prepare students to improvise on this relatively simple implementation as teams approach CIS 412.

## Submitting work
Lab reports will be submitted by 
1. Generating a markdown file in the labreports directory under the naming convention: **LAB_[GITHUB HANDLE].md**, 
2. Submitting a Pull Request to this repository that include your lab report as well as any accompanying images/files (there are diagrams required in the lab content), and 
3. Providing the URL for that pull request in the Canvas/LMS platform

* Throughout these instructions, you'll find that **items marked in bold text** reference content you are to submit in your lab report.
* For the purposes of clear communication, you may base your lab report off of the template found in [LAB.md](LAB.md), but you're also free, welcome, and encouraged to get more creative.
* If you are unfamiliar with markdown, I recommend checking [1000 places on the Interwebs](http://lmgtfy.com/?q=learn+markdown) that will help you close that gap.

# Step 0: Installing appropriate tools / logins
1. If you don't have a GitHub account already, [create one](https://github.com/join). 
2. [Install _git_](https://git-scm.com/downloads) on your development environment.
3. Install a text editor or some sort of application for local development. Lately, I'm partial to [Visual Studio Code](https://code.visualstudio.com/) and my instructions assume it's use, but you're welcome to diviate. _Each one should choose their own sword, etc. etc._
4. Install Docker on your development environment, either for [Mac](https://docs.docker.com/docker-for-mac/install/), [Windows](https://docs.docker.com/docker-for-windows/install/), or various Linux distributions.
5. [Signup for an account on Docker Hub](https://hub.docker.com/) and keep track of your username and password (You'll need that later).
6. [Signup for a Heroku](https://signup.heroku.com) account (You'll need that later too).
7. [Download and install the Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli#download-and-install).


# Step 1: Fork and clone this repository
1. After logging in, navigate to the [root](https://github.com/tangollama/cis411_lab2) of this repository.
2. Fork this repository to your personal GitHub account (hint: read the page).
3. Navigate to your forked repository in your GitHub account and copy the reference to your repository in from the <button>Clone or Download</button> button.
4. Open the terminal or command line interface on your development machine, navigate to your chosen working directory, and execute the following command: 
```
> git clone [YOUR COPIED GITHUB CLONE REFERENCE]
```

5. Navigate to that directory 
```
> cd cis411_lab2
```

6. Run npm install and watch the magic happen.
```
> npm install
``` 

7. Run the command below and navigate to [http://localhost:4000/graphql](http://localhost:4000/graphql) in a web browser.
```
> npm start
``` 

8. Verify that you can see the GraphiQL interface and shut down the server with the use of ```Ctrl+C``` in the command line window that is currently running the ```npm start``` command.

# Step 2: Setup a Continuous Integration configuration
1. [Signup for CircleCI](https://circleci.com/signup/) with your GitHub account.
2. Login to CircleCI and add your project to your account (ex. https://circleci.com/add-projects/gh/[YOUR_GITHUB_HANDLE]) by clicking _Add Project_ and selecting your forked repository for cis411_lab2.
3. Follow the setup instructions, including creating the .circleci directory and adding the default config.yml file.
![CircleCI setup](../assets/circleci_setup.png "CircleCI Setup")
- Create a directory name .circleci in your project 
```
> mkdir .circleci
```
- Add a file to that directory named config.yml ```code .circleci/config.yml```.
- Copy the content for the setup instructions into config.yml.
4. Add the  .circleci directory to your forked repository. **Note: these files must be present in your submitted pull request.**
```
> git add .circleci
> git commit -m "something something something"
> git push
```
5. Verify that the current config file is correct and the project is building in CircleCI.

# Step 3: Create a Dockerfile and run docker commands
1. Create a file in the **root directory** of your repository called **Dockerfile**.
2. Add the following content to that file and save it:
```
FROM node:11
WORKDIR /dist
COPY package.json /dist
RUN npm install
COPY . /dist
CMD node server.js
EXPOSE 4000
```
3. Run the following command:
```
> docker login
```
4. Provide your Docker Hub username and password
5. Build and run the Docker image using the following commands from _within_ the cis411_lab2 directory:
```
> docker build -t lab2 .
> docker run -p 4000:4000 lab2 &
```
6. Navigate to http://localhost:4000/graphql and verify that you can access GraphiQL.
7. Shutdown the docker container by running the following command: 
```
> docker stop $(docker ps -aq)
```
8. Add the related **Dockerfile** to your forked repository. **This file must be present in your submitted pull request.**
```
> git add Dockerfile
> git commit -m "something something something Docker something"
> git push
```

9. **Answer the following in your lab report**: why would a containerized version of an application be beneficial if you can run the application locally already?

# Step 4: Setup a Heroku application
There are _lots_ of solutions for providing a CD endpoint including AWS, Google Cloud, Asure, Digital Ocean, etc. For the purposes of this assignment, we're going to use **Heroku** for one reason: it's _relatively_ easy.

1. Login to heroku through the CLI using the username and password you created when you signed up for an account.
```
> heroku login
```
2. Initiate a Heroku app. This can be handled through [the user interface](http://heroku.com/deploy) or via the command line instructions below, replacing the [GITHUB_HANDLE] with your GitHub handle.
```
> heroku apps:create cis411lab2-[GITHUB_HANDLE] -b heroku/nodejs
> git push heroku master 
```
You should see quite a bit of output as the application builds itself and deploys to Heroku.

3. Open a web browser and go to the following URL to ensure your app is running:
```
http://[GITHUB_HANDLE].herokuapp.com/graphql
```
4. Include this URL in your lab report. 

# Step 5: Configure CircleCI for Docker and Heroku

1. Run the following command to generate a Heroku API tokem:
```
heroku authorizations:create -d "CIS411 Lab token something something"
```
You should see a response that looks like this.
```
Creating OAuth Authorization... done
Client:      <none>
ID:          xxxxxx-xxxx-xxx-xxxx-xxxxxxxx
Description: CIS411 Lab token something something
Scope:       global
Token:       xxxxxx-xxxxx-xxxx-xxxx-xxxxxxx
Updated at:  Tue Nov 13 2018 23:53:14 GMT-0500 (Eastern Standard Time) (less than a minute ago)
```

2. [Open the CircleCI](https://circleci.com/dashboard) user interface and navigate to: 
```
Settings > Projects > [Click on the Gear icon in the far right corner of this project] > Environment Variables
```

3. Add the following two environment variables to CircleCI: HEROKU_API_KEY equal to the Token generated from the command above and HEROKU_APP_NAME equal to the name of your Heroku app: cis411lab2-[GITHUB_HANDLE].
![HEROKU_APP_NAME](../assets/ci_app_name.png "HEROKU_APP_NAME")

![HEROKU_API_KEY](../assets/ci_api_key.png "HEROKU_API_KEY")

2. Open the ```.circleci/config.yml``` file and add the following contents to the end of the file:
```
  deploy:
    docker:
      - image: buildpack-deps:trusty
    steps:
      - checkout
      - run:
          name: Deploy Master to Heroku
          command: |
            git push https://heroku:$HEROKU_API_KEY@git.heroku.com/$HEROKU_APP_NAME.git master

workflows:
  version: 2
  build-deploy:
    jobs:
      - build
      - deploy:
          requires:
            - build
          filters:
            branches:
              only: master
```