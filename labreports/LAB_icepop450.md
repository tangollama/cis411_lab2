# Lab Report Template for CIS411_Lab2
Course: Messiah College CIS 411, Fall 2019

Instructors: [Joel Worrall](https://github.com/tangollama) & [Trevor Bunch](https://github.com/trevordbunch)

Name: Issac Houck

GitHub: [icepop450](https://github.com/icepop450)

# Required Content

1. Generate a markdown file in the labreports directoy named LAB_[GITHUB HANDLE].md. Write your lab report there.
2. Create the directory ```./circleci``` and the file ```.circleci/config.yml``` in your project and push that change to your GitHub repository.
3. Create the file ```Dockerfile``` in the root of your project and include the contents of the file as described in the instructions. Push that change to your GitHub repository.
4. Write the URL of your running Heroku app here: http://cis411lab2-icepop450.herokuapp.com/graphql
5. Embed _using markdown_ a screenshot of your successful build and deployment to Heroku of your project.
!["circleci test"](../circleci_test.PNG)
!["heroku app"](../herokuapp.PNG)
6. Answer the questions below.
7. Submit a Pull Request to cis411_lab2 and provide the URL of that Pull Request in Canvas as your URL submission.

## Questions
1. Why would a containerized version of an application be beneficial if you can run the application locally already?
    A contanerized application is beneficial when more than one person is using it or its being used on different machines in some way.  Because it will ensure that the application will run the same no matter where its used.
2. If we have the ability to publish directory to Heroku, why involve a CI solution like CircleCI? What benefit does it provide?
    CircleCI helps to make the code more reliable so that faulty code will not get pushed to master as often.  This can save a lot of time with finding bugs and increases reliability which is always very beneficial.
