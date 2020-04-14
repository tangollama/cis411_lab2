# Lab Report Template for CIS411_Lab2
Course: Messiah College CIS 411, Fall 2018

Instructors: [Joel Worrall](https://github.com/tangollama) & [Trevor Bunch](https://github.com/trevordbunch)

Name: YOUR NAME

GitHub: [@drewpoo99](https://github.com/drewpoo99)

# Required Content

[x] 1. Generate a markdown file in the labreports directoy named LAB_[GITHUB HANDLE].md. Write your lab report there.
[x] 2. Create the directory ```./circleci``` and the file ```.circleci/config.yml``` in your project and push that change to your GitHub repository.
[x] 3. Create the file ```Dockerfile``` in the root of your project and include the contents of the file as described in the instructions. Push that change to your GitHub repository.
[x] 4. Write the URL of your running Heroku app here: ```http://cis411lab2-drewpoo99.herokuapp.com/graphql```
[x]5. ![image](https://github.com/drewpoo99/cis411_lab2/blob/master/assets/drewpoo99-circleci-failed.png)
[x]7. Submit a Pull Request to cis411_lab2 and provide the URL of that Pull Request in Canvas as your URL submission.

## Questions
1. Why would a containerized version of an application be beneficial if you can run the application locally already?
    Containerization allows for the app to be scalable for users without wasting resources. If lots of users want to use the app at once, more containers can be replicated to serve those users, then when they are done using the app those containers can be turned off so the resources aren't being used for nothing.
2. If we have the ability to publish directory to Heroku, why involve a CI solution like CircleCI? What benefit does it provide?
    CI is important because it allows us to set up tests and other functions when deploying to make sure our app is able to function and get deployed well. It can act as a saftey net when we deploy because depending on the automated testing that we have set up, it can let us know when an update to the repository is not working with currently deployed software. CI can do lots of other things too, I'm sure.
