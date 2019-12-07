# Lab Report Template for CIS411_Lab2
Course: Messiah College CIS 411, Fall 2018

Instructors: [Joel Worrall](https://github.com/tangollama) & [Trevor Bunch](https://github.com/trevordbunch)

Name: YOUR NAME

GitHub: [Andrekerlin](https://github.com/AndreKerlin)

# Required Content

1. Generate a markdown file in the labreports directoy named LAB_[GITHUB HANDLE].md. Write your lab report there.
2. Create the directory ```./circleci``` and the file ```.circleci/config.yml``` in your project and push that change to your GitHub repository.
3. Create the file ```Dockerfile``` in the root of your project and include the contents of the file as described in the instructions. Push that change to your GitHub repository.
4. Write the URL of your running Heroku app here: http://andrekerlin.herokuapp.com/graphql
5. Embed _using markdown_ a screenshot of your successful build and deployment to Heroku of your project.
![CircleCi(lab2image.png "screenshot of circleci attempts")
6. Answer the questions below.
7. Submit a Pull Request to cis411_lab2 and provide the URL of that Pull Request in Canvas as your URL submission.


## Questions
1. Why would a containerized version of an application be beneficial if you can run the application locally already?
-a contanerized version of the application would avoid the need to launch with a virtual machine, making development a lot faster as well as scaling since we can edit aspects of it instead of the entire application.
2. If we have the ability to publish directory to Heroku, why involve a CI solution like CircleCI? What benefit does it provide?
-CircleCI tests everything before we commit it while heroku does not.