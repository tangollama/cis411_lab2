# Lab Report Template for CIS411_Lab2
Course: Messiah College CIS 411, Fall 2018

Instructors: [Joel Worrall](https://github.com/tangollama) & [Trevor Bunch](https://github.com/trevordbunch)

Name: Michael Williams

GitHub: [mw1421](https://github.com/mw1421)

# Required Content

1. Generate a markdown file in the labreports directoy named LAB_[GITHUB HANDLE].md. Write your lab report there.
2. Create the directory ```./circleci``` and the file ```.circleci/config.yml``` in your project and push that change to your GitHub repository.
3. Create the file ```Dockerfile``` in the root of your project and include the contents of the file as described in the instructions. Push that change to your GitHub repository.
4. Write the URL of your running Heroku app here: ```ex: http://cis411lab2-mw1421.herokuapp.com/graphql```
5. Embed _using markdown_ a screenshot of your successful build and deployment to Heroku of your project.
6. Answer the questions below.
7. Submit a Pull Request to cis411_lab2 and provide the URL of that Pull Request in Canvas as your URL submission.

## Questions
1. Why would a containerized version of an application be beneficial if you can run the application locally already?

Being able to use the application without spinning it up first is good. Instead of going into a command-line and using npm start and then going to localhost:4000/graphql, you can just use the web url to use the same application. 

2. If we have the ability to publish directory to Heroku, why involve a CI solution like CircleCI? What benefit does it provide?

It helps to check if problems are occuring or not. When you are building an application with many different developers pushing to the same repository, it can become cluttered for what is actually working and what is not. Being able to have an application automate that process is very beneficial to have, instead of manually trying to find which commit-push combo broke the application. 

![GraphQL on Heroku](https://drive.google.com/file/d/1E3TPAzusJV-BpVVVkiIB3bMJXcnSJPJh/view?usp=sharing "GraphQL on Heroku")

![CircleCI build check](https://drive.google.com/file/d/1872og9zx-nVkrfkCNYLmFWjs7fs9kjlq/view?usp=sharing "CircleCI build check")