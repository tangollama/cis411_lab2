# Lab Report for CIS411_Lab2
Course: Messiah College CIS 411, Fall 2018

Instructors: [Joel Worrall](https://github.com/tangollama) & [Trevor Bunch](https://github.com/trevordbunch)

Name: Ben Underwood

GitHub: [benunderw](https://github.com/benunderw)

# Required Content

1. Generate a markdown file in the labreports directoy named LAB_benunderw.md. Write your lab report there.
2. Create the directory ```./circleci``` and the file ```.circleci/config.yml``` in your project and push that change to your GitHub repository.
3. Create the file ```Dockerfile``` in the root of your project and include the contents of the file as described in the instructions. Push that change to your GitHub repository.
4. Write the URL of your running Heroku app here: http://cis411lab2-benunderw.herokuapp.com/graphql
5. Embed _using markdown_ a screenshot of your successful build and deployment to Heroku of your project.
![CircleCI build and deployment to Heroku](https://i.imgur.com/KoRjywn.png)
6. Answer the questions below.
7. Submit a Pull Request to cis411_lab2 and provide the URL of that Pull Request in Canvas as your URL submission.

## Questions
1. Why would a containerized version of an application be beneficial if you can run the application locally already?

A container allows for application-specific packages and settings to be easily customized and deployed to other environments without much hassle. It's easier to give someone a dockerfile than to tell them to manually install a bunch of packages to get your app to run.

2. If we have the ability to publish directory to Heroku, why involve a CI solution like CircleCI? What benefit does it provide?

Continuous Integration allows us to easily build, test, and deploy applications to hosts like Heroku in a seamless/efficient manner. Automating these tasks frees up more time to spend adding features and fixing bugs in the application rather than in our build environment.
