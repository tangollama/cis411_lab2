# Lab Report Template for CIS411_Lab2
Course: Messiah College CIS 411, Fall 2018

Instructors: [Joel Worrall](https://github.com/tangollama) & [Trevor Bunch](https://github.com/trevordbunch)

Name: Stephanie Tran

GitHub: [tran1996](https://github.com/tran1996)

# Required Content

1. Generate a markdown file in the labreports directoy named LAB_[GITHUB HANDLE].md. Write your lab report there.

2. Create the directory ```./circleci``` and the file ```.circleci/config.yml``` in your project and push that change to your GitHub repository.

3. Create the file ```Dockerfile``` in the root of your project and include the contents of the file as described in the instructions. Push that change to your GitHub repository.
4. Write the URL of your running Heroku app here: https://cis411lab2-tran1996.herokuapp.com/graphql

5. Embed _using markdown_ a screenshot of your successful build and deployment to Heroku of your project.
![alt text](https://github.com/tran1996/cis411_lab1/blob/master/labreports/heroku.png "Heroku")

## Questions
1. Why would a containerized version of an application be beneficial if you can run the application locally already?
    Having a version of an app running in a container would eliminate the chances of errors when a variety of people are using machines with different configurations. Even if the actual machine is different, this lets all the team members develop the app on similar virtual machines.  

2. If we have the ability to publish directory to Heroku, why involve a CI solution like CircleCI? What benefit does it provide?
    CI solutions, like CircleCi, would allow us to test the app to see whether or not it works or is successful before actually deploying it.