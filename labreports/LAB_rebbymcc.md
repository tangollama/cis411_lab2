# Lab Report Template for CIS411_Lab2
Course: Messiah College CIS 411, Fall 2018

Instructors: [Joel Worrall](https://github.com/tangollama) & [Trevor Bunch](https://github.com/trevordbunch)

Name: Rebekah McClelland

GitHub: rebbymcc(https://github.com/rebbymcc)

# Required Content

1. Generate a markdown file in the labreports directoy named LAB_[GITHUB HANDLE].md. Write your lab report there.
2. Create the directory ```./circleci``` and the file ```.circleci/config.yml``` in your project and push that change to your GitHub repository.
3. Create the file ```Dockerfile``` in the root of your project and include the contents of the file as described in the instructions. Push that change to your GitHub repository.
4. Write the URL of your running Heroku app here: http://[rebbymcc.herokuapp.com/graphql]```ex: http://[cis411lab2-tangollama.herokuapp.com/graphql```
5. Embed _using markdown_ a screenshot of your successful build and deployment to Heroku of your project.
  [Screenshot of successful build](https://github.com/rebbymcc/cis411_lab2/blob/master/success.png)
6. Answer the questions below.
7. Submit a Pull Request to cis411_lab2 and provide the URL of that Pull Request in Canvas as your URL submission.

## Questions
1. Why would a containerized version of an application be beneficial if you can run the application locally already?
A containerized version of an application would be beneficial because everything is located in one specific designated place and would therefore be much easier to debug and trouble shoot when the need arises.  Then when it finally is running as it should it can be deployed so that it does not hinder anything not within the app itself. 
2. If we have the ability to publish directory to Heroku, why involve a CI solution like CircleCI? What benefit does it provide?
A CI solution like CircleCI is helpful because it tells you when a build fails, why the build fails and this makes it much easier to find and fix problems within your application.
