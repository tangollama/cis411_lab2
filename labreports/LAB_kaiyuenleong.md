# Lab Report Template for CIS411_Lab2
Course: Messiah College CIS 411, Fall 2018

Instructors: [Joel Worrall](https://github.com/tangollama) & [Trevor Bunch](https://github.com/trevordbunch)

Name: Kai Yuen Leong

GitHub: [kaiyuenleong](https://github.com/kaiyuenleong)

# Required Content

1. Generate a markdown file in the labreports directoy named LAB_kaiyuenleong.md. Write your lab report there. (COMPLETE)
2. Create the directory ```./circleci``` and the file ```.circleci/config.yml``` in your project and push that change to your GitHub repository. (COMPLETE)
3. Create the file ```Dockerfile``` in the root of your project and include the contents of the file as described in the instructions. Push that change to your GitHub repository. (COMPLETE)
4. Write the URL of your running Heroku app here: ```http://cis411lab2-kaiyuenleong.herokuapp.com/graphql``` 
5. Embed _using markdown_ a screenshot of your successful build and deployment to Heroku of your project.  
![successful build](https://github.com/kaiyuenleong/cis411_lab2/blob/master/labreports/successful_build.jpg "CircleCI successful build")
6. Answer the questions below. (COMPLETE)
7. Submit a Pull Request to cis411_lab2 and provide the URL of that Pull Request in Canvas as your URL submission. (COMPLETE)

## Questions
1. Why would a containerized version of an application be beneficial if you can run the application locally already? **A containerized version of an application keeps all the application code dependencies together. If one were to test the application on an external platform, it will be easier to ship all the application code along with its dependencies as one package rather than needing to track down every component.**

2. If we have the ability to publish directory to Heroku, why involve a CI solution like CircleCI? What benefit does it provide? **CircleCI is a Continuous Integration tool that checks the repository of an application each time new/modified code is pushed to the repository to automatically verify that the integrity of the repository is maintained. By involving CI tools like CircleCI to automatically check that an application build is properly integrated, the integration process can be sped up so that developers can deploy applications through utilities like Heroku much more quickly.**
