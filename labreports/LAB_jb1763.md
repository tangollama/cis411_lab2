# Lab Report Template for CIS411_Lab2
Course: Messiah College CIS 411, Fall 2018

Instructors: [Joel Worrall](https://github.com/tangollama) & [Trevor Bunch](https://github.com/trevordbunch)

Name: Jared Butler

GitHub: [jb1763](https://github.com/jb1763)

# Required Content

1. Generate a markdown file in the labreports directoy named LAB_[GITHUB HANDLE].md. Write your lab report there.
2. Create the directory ```./circleci``` and the file ```.circleci/config.yml``` in your project and push that change to your GitHub repository.
3. Create the file ```Dockerfile``` in the root of your project and include the contents of the file as described in the instructions. Push that change to your GitHub repository.
4. Write the URL of your running Heroku app here: [https://cis411lab2-jb1763.herokuapp.com/graphql](https://cis411lab2-jb1763.herokuapp.com/graphql)```ex: http://[cis411lab2-tangollama.herokuapp.com/graphql```
5. Embed _using markdown_ a screenshot of your successful build and deployment to Heroku of your project.
![Successful build and deployment of heroku project](../img/herokubuild.png)
6. Answer the questions below.
7. Submit a Pull Request to cis411_lab2 and provide the URL of that Pull Request in Canvas as your URL submission.

## Questions
1. Why would a containerized version of an application be beneficial if you can run the application locally already?
You can ensure that your environment is identical to the environment the application will run in.
You can ensure that there aren't dependencies outside of what you expect.
You can be sure everyone can test in the same environment.

2. If we have the ability to publish directory to Heroku, why involve a CI solution like CircleCI? What benefit does it provide?
It serves as a staging environment.
We can ensure that the application passes all test cases before we deploy.
Devs can see results of test very shortly after committing code.
