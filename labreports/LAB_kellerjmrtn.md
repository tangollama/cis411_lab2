# Lab Report Template for CIS411_Lab2
Course: Messiah College CIS 411, Fall 2018

Instructors: [Joel Worrall](https://github.com/tangollama) & [Trevor Bunch](https://github.com/trevordbunch)

Name: YOUR NAME

GitHub: [kellerjmrtn](https://github.com/kellerjmrtn)

# Required Content

1. Generate a markdown file in the labreports directoy named LAB_[GITHUB HANDLE].md. Write your lab report there.
2. Create the directory ```./circleci``` and the file ```.circleci/config.yml``` in your project and push that change to your GitHub repository.
3. Create the file ```Dockerfile``` in the root of your project and include the contents of the file as described in the instructions. Push that change to your GitHub repository.
4. Write the URL of your running Heroku app here: ```http://cis411lab2-kellerjmrtn.herokuapp.com/graphql```
5. Embed _using markdown_ a screenshot of your successful build and deployment to Heroku of your project: [CircleCi Build](../images/build.png), [Heroku Deployment (cmd line)](../images/deploy.png), and [Heroku Deployment (browser)](../images/deploy-browser.png)
6. Answer the questions below.
7. Submit a Pull Request to cis411_lab2 and provide the URL of that Pull Request in Canvas as your URL submission.

## Questions
1. **Why would a containerized version of an application be beneficial if you can run the application locally already?**
    Anyone using the container will be running on the exact same environment, even if they are using different computers/hardware or operating systems. This helps to standardize its use and helps with debugging/preventing errors. 
2. **If we have the ability to publish directory to Heroku, why involve a CI solution like CircleCI? What benefit does it provide?**
    CircleCi can run tests to help monitor our code. This helps keep the code error free (ideally) and running smoothly.
