# Lab Report CIS411_Lab2
Course: Messiah College CIS 411, Fall 2018

Instructors: [Joel Worrall](https://github.com/tangollama) & [Trevor Bunch](https://github.com/trevordbunch)

Name: Donovan Varney

GitHub: [dv1187](https://github.com/dv1187)

# Required Content

1. Generate a markdown file in the labreports directoy named LAB_[GITHUB HANDLE].md. Write your lab report there. ✅
2. Create the directory ```./circleci``` and the file ```.circleci/config.yml``` in your project and push that change to your GitHub repository. ✅
3. Create the file ```Dockerfile``` in the root of your project and include the contents of the file as described in the instructions. Push that change to your GitHub repository. ✅
4. Write the URL of your running Heroku app here: ```http://cis411lab2-dv1187.herokuapp.com/graphql``` ✅
5. Embed _using markdown_ a screenshot of your successful build and deployment to Heroku of your project. ✅
![Screenshot Here](https://github.com/dv1187/cis411_lab2/blob/master/assets/screenshot.png "Successful Build")
6. Answer the questions below. ✅
7. Submit a Pull Request to cis411_lab2 and provide the URL of that Pull Request in Canvas as your URL submission. ✅

## Questions
1. Why would a containerized version of an application be beneficial if you can run the application locally already?
	`There are several pros to running a containerized version of an app. A containerized app is less resource-intensive than running virtual machines, which in turn means that you can create more heavier workload applications on the same server. Using containers also decreases the amount of time it takes to test and deploy applications and services.`
2. If we have the ability to publish directory to Heroku, why involve a CI solution like CircleCI? What benefit does it provide?
	`CI solutions are helpful to use between builds to figure out whether or not a developer broke one of the parts of the application with the most recent push. If it broke, it has a bright red WARNING button that shows developers that something was broken and needs to be addressed. If nothing broke, everyone celebrates because a green SUCCESS button shows itself.`