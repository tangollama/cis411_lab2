# Lab Report Template for CIS411_Lab2
Course: Messiah College CIS 411, Fall 2018

Instructors: [Joel Worrall](https://github.com/tangollama) & [Trevor Bunch](https://github.com/trevordbunch)

Name: Garrett Reichert

GitHub: g-reichert(https://github.com/g-reichert)

# Required Content

1. Generate a markdown file in the labreports directoy named LAB_g-reichert.md. Write your lab report there.
2. Create the directory ```./circleci``` and the file ```.circleci/config.yml``` in your project and push that change to your GitHub repository.
3. Create the file ```Dockerfile``` in the root of your project and include the contents of the file as described in the instructions. Push that change to your GitHub repository.
4. Write the URL of your running Heroku app here: ```http://cis411lab2-g-reichert.herokuapp.com/graphql```
5. Embed _using markdown_ a screenshot of your successful build and deployment to Heroku of your project.
![alt text](https://github.com/g-reichert/cis411_lab2/blob/master/lab2pic2.png "Step 5")
6. Answer the questions below.
7. Submit a Pull Request to cis411_lab2 and provide the URL of that Pull Request in Canvas as your URL submission.

## Questions
1. Why would a containerized version of an application be beneficial if you can run the application locally already?

Container technology is a method to package an application so it can be run, with its dependencies, isolated from other processes. The great part about container technology is that we can ship it around with out being concerened that it will break in a new environemnt, since we are just moving the container from place to place. The benefit is that by making a containerized version of the application, we will know that it will run wherever we move it to, and we don't need to be concerened about it breaking when we move it.

2. If we have the ability to publish directory to Heroku, why involve a CI solution like CircleCI? What benefit does it provide?

A continuous intergration tool allows us to test to make sure that everything is working when we check in. While we can publish straight to Heroku, that doesn't check to make sure that our code is still working as expected.
