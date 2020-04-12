# Lab Report Template for CIS411_Lab2
Course: Messiah College CIS 411, Fall 2018

Instructors: [Joel Worrall](https://github.com/tangollama) & [Trevor Bunch](https://github.com/trevordbunch)

Name: Bryce Doane

GitHub: [BryceDoane](https://github.com/BryceDoane)

# Required Content

1. Generate a markdown file in the labreports directoy named LAB_[GITHUB HANDLE].md. Write your lab report there.
2. Create the directory ```./circleci``` and the file ```.circleci/config.yml``` in your project and push that change to your GitHub repository.
3. Create the file ```Dockerfile``` in the root of your project and include the contents of the file as described in the instructions. Push that change to your GitHub repository.
4. Write the URL of your running Heroku app here: ``http://brycedoane.herokuapp.com/graphql``
5. Embed _using markdown_ a screenshot of your successful build and deployment to Heroku of your project.
    ![](screenshot.png)
6. Answer the questions below.
7. Submit a Pull Request to cis411_lab2 and provide the URL of that Pull Request in Canvas as your URL submission.

## Questions
1. Why would a containerized version of an application be beneficial if you can run the application locally already?

    <b> Containers allow us, as developers, to change the 
environment that the application runs in, which cannot be done or is harder to do locally.  Also, containers are very efficient with resources and easy to use.  They can be created when needed then go away when they aren't, freeing up computing resources.

2. If we have the ability to publish directory to Heroku, why involve a CI solution like CircleCI? What benefit does it provide?

    <b> CircleCI provides some services that Heroku doesn't, such as testing the application and debug functions.  CircleCI is also built for continuous integration and deployment and is an additional step that allows developers to test the build across multiple containers. 