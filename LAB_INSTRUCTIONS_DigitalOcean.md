# CIS 411 Lab 4: GitHub + Docker + CircleCI + Digital Ocean
The purpose of this lab is to get hands on experience working with Docker, CircleCI, and a Cloud Service Provider like Digital Ocean to create a CI/CD pipeline. Though the lab is generally paint by numbers, the hands on experience with the tools is meant to prepare students to improvise on this relatively simple implementation as teams approach CIS 471.

## Submitting work
Lab reports will be submitted by 
1. Generating a markdown file in the `labreports` directory under the naming convention: **LAB_[GITHUB HANDLE].md**, 
2. Submitting a Pull Request to this repository that include your lab report as well as any accompanying images/files (there are diagrams required in the lab content), and 
3. Providing the URL for that pull request in the Canvas/LMS platform

* Throughout these instructions, you'll find that **items marked in bold text** reference content you are to submit in your lab report.
* For the purposes of clear communication, you may base your lab report off of the template found in [LAB_Template.md](/labreports/LAB_Template.md), but you're also free, welcome, and encouraged to get more creative.

# Step 0: Installing appropriate tools / logins
1. If you don't have a GitHub account already, [create one](https://github.com/join). 
2. [Install _git_](https://git-scm.com/downloads) on your development environment.
3. Install a text editor or some sort of application for local development. Lately, I'm partial to [Visual Studio Code](https://code.visualstudio.com/) and my instructions assume it's use, but you're welcome to deviate. _Each one should choose their own sword, etc. etc._
4. Install Docker on your development environment, either for [Mac](https://docs.docker.com/docker-for-mac/install/), [Windows](https://docs.docker.com/docker-for-windows/install/), or various Linux distributions.  
> If you have Windows Home Edition, then you should following these [instructions](ex/Docker_Installation_Win10_Home.md) to navigate the system requirements.  
5. [Sign up for an account on Docker Hub](https://hub.docker.com/) and keep track of your username and password (You'll need that later).
6. [Sign up for a Digital Ocean](https://www.digitalocean.com/) account. You will need to add a card to get the free credits. 


# Step 1: Fork and clone this repository
1. After logging in, navigate to the [root](https://github.com/trevordbunch/cis411_lab4_CD) of this repository.
2. Fork this repository to your personal GitHub account (hint: read the page).
3. Navigate to your forked repository in your GitHub account and copy the reference to your repository in from the <button>Clone or Download</button> button.
4. Open the terminal or command line interface on your development machine, navigate to your chosen working directory, and execute the following command: 
```
> git clone [YOUR COPIED GITHUB CLONE REFERENCE]
```

5. Navigate to that directory 
```
> cd cis411_lab4_CD
```

6. Run npm install and watch the magic happen.
```
> npm install
``` 

7. Run the command below and navigate to [http://localhost:4000/graphql](http://localhost:4000/graphql) in a web browser.
```
> npm start
``` 

1. Verify that you can see the GraphQL interface and shut down the server with the use of ```Ctrl+C``` in the command line window that is currently running the ```npm start``` command.


# Step 2: Setup a Continuous Integration configuration
1. [Login into CircleCI](https://circleci.com/vcs-authorize/) or [Sign up to CircleCI](https://circleci.com/signup/) with your GitHub account.
2. Login to CircleCI and add your project to your account (ex. https://circleci.com/add-projects/gh/[YOUR_GITHUB_HANDLE]) by clicking _Add Project_ and selecting your forked repository for cis411_lab4_CD.
3. Follow the setup instructions, including creating the .circleci directory and adding the content below to a config.yml file.
![CircleCI setup](assets/circleci_setup.png "CircleCI Setup")
- Create a directory name .circleci in your project 
```
> mkdir .circleci
```
- Add a file to that directory named config.yml ```code .circleci/config.yml```.
- Copy the content below into config.yml.
```
version: 2
jobs:
  build:  
    docker:
      - image: circleci/node:11
    steps:
      - checkout

      # Download and cache dependencies
      - restore_cache:
          keys:
          - v1-dependencies-{{ checksum "package.json" }}
          # fallback to using the latest cache if no exact match is found
          - v1-dependencies-

      - run: yarn install

      - save_cache:
          paths:
            - node_modules
          key: v1-dependencies-{{ checksum "package.json" }}
        
      # run tests!
      - run: yarn test
```
1. Save and add the .circleci directory to your forked repository. **Note: these files must be present in your submitted pull request.**
```
> git add .circleci
> git commit -m "something something something"
> git push
```
5. Verify that the current config file is correct and the project is building in CircleCI.

# Step 3: Create a Dockerfile and run docker commands
1. Create a file in the **root directory** of your repository called **Dockerfile** (no file extension).
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
5. Build and run the Docker image using the following commands from _within_ the cis411_lab4_CD directory:
```
> docker build -t lab4 .
> docker run -p 4000:4000 lab4 &
```
> Tip: the period (`.`) at the end of the command is important!  
6. Navigate to http://localhost:4000/graphql and verify that you can access GraphQL.
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

# Step 4: Push docker desktop file to docker hub
Docker desktop is different than docker hub, you must push your image to your docker hub account. Do the following from git cli:
1. Tag your image
  ```docker tag your-local-image your-docker-hub-username/repository-name:tag```<br> 
    Example
  ```docker tag lab4 rt1252/lab4:tag```
2. Push to docker hub
   ```docker push your-docker-hub-username/repository-name:tag``` <br>
   Example
   ```docker push rt1252/lab4:tag```
3. Go to [docker hub](https://hub.docker.com/repositories) and view your repo.

# Step 5: Setup a Digital Ocean application
There are _lots_ of solutions for providing a CD endpoint including AWS, Google Cloud, Azure, Digital Ocean, etc. For the purposes of this assignment, we're going to use **Digital Ocean** for one reason: it's _relatively_ easy. They provide $200 free credits which must be used in 60 days.

1. Login to [Digital Ocean](https://cloud.digitalocean.com/projects?i=49cc11) through the web interface and click create then click app.
![Create app](/assets/do1.png)
2. Select the docker hub option and enter your repo copying the name from the command above. Enter 'tag' for tag. You should also [see your docker hub repo here](https://hub.docker.com/).
![Select docker hub](/assets/do2.png)
3. Click next accepting the default settings, when you get to info you can change the name of the app to cis411lab4-[GITHUB_HANDLE]. Click create resources. 
4. Wait for service to deploy.
5. Click the live app button and append /graphql to the end. You will see graphql running!  
 ![Live Application](assets/digitalOcean_success.png) 
6. **Include this URL in your lab report.**

# Step 6: Configure CircleCI for CD to Digital Ocean

1. From the menu on the digital ocean homepage scroll to the bottom and click API. 
![api](/assets/do3.png)
   
2. Click the generate new token button, name the token, and click generate, copy the token.
![api_key](assets/digitalOcean_api_key.png)

3. [Open the CircleCI](https://circleci.com/dashboard) user interface and navigate to: 
```
Settings > Projects > [Click on the Gear icon in the far right corner of this project] > Environment Variables
```

4. Add the following two environment variables to CircleCI: OCEAN_API_KEY equal to the Token generated from the command above and OCEAN_APP_NAME equal to the name of your digital ocean app: cis411lab4-[GITHUB_HANDLE]. Change the information in the screenshots to show what it would look like for Digital Ocean (as described above).
![OCEAN_APP_NAME](/assets/ev1.png)
![OCEAN_API_KEY](assets/ev2.png)

5. Open the ```.circleci/config.yml``` file and add the following contents to the end of the file:
```
deploy:
    docker:
      - image: buildpack-deps:trusty
    steps:
      - checkout
      - run:
          name: Install dependencies
          command: |
            sudo apt-get update
            sudo apt-get install -y python3-pip
            pip3 install awscli
            curl -sL https://deb.nodesource.com/setup_14.x | sudo -E bash -
            sudo apt-get install -y nodejs
      - run:
          name: Install doctl
          command: |
            wget https://github.com/digitalocean/doctl/releases/download/v1.64.0/doctl-1.64.0-linux-amd64.tar.gz
            tar xf doctl-1.64.0-linux-amd64.tar.gz
            sudo mv doctl /usr/local/bin
            rm doctl-1.64.0-linux-amd64.tar.gz
      - run:
          name: Authenticate with DigitalOcean
          command: |
            doctl auth init --access-token $OCEAN_API_KEY
            doctl kubernetes cluster kubeconfig save mycluster
            kubectl config use-context do-myapp
      - run:
          name: Deploy to DigitalOcean
          command: |
            kubectl apply -f k8s

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
              only: main
```
> **TIP:** The indentation is important to how CircleCI understands how to interpret the commands.  Notice that the deployment commands are only applied to the `main` branch.

6. Commit and save those changes and push them to your GitHub repository.
```
> git add *
> git commit -m "Changes something something"
> git push origin master
```
7. Login to CircleCI and **take a screenshot of the successful build and deployment** of your application to Digital Ocean.
![Success](assets/digitalOcean_circleci2.png)

8. Open up your deployed application on Digital Ocean and register your account using the following Graphql mutation:
```
mutation {
  mutateAccount(input: {
    email: "YOUR EMAIL"
    name: "YOUR FULL NAME"
    mutation: "add"
  }) {
    id
    name
    email
  }
}
```

# Step 6: Reflection / Feedback
Answer the following 4 questions in your [Lab Report](/labreports/LAB_Template.md): 
1. Why would a containerized version of an application be beneficial if you can run the application locally already?
2. If we have the ability to publish directory to Heroku, why involve a CI solution like CircleCI? What benefit does it provide?
3. Why would you use a container technology over a virtual machine(VM)?
4. What are some alternatives to Docker for containerized deployments?

# Step 7: Submit your work
Complete a pull request to the source repository and use the PR URL to submit your assignment in canvas.
