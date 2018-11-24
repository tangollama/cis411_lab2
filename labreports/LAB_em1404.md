# Lab Report Template for CIS411_Lab2
Course: Messiah College CIS 411, Fall 2018

Instructors: [Joel Worrall](https://github.com/tangollama) & [Trevor Bunch](https://github.com/trevordbunch)

Name: Eliezer Mwankenja

GitHub: [em1404](https://github.com/em1404)

# Required Content

1. Generate a markdown file in the labreports directoy named LAB_[GITHUB HANDLE].md. Write your lab report there.
2. Create the directory ```./circleci``` and the file ```.circleci/config.yml``` in your project and push that change to your GitHub repository.
3. Create the file ```Dockerfile``` in the root of your project and include the contents of the file as described in the instructions. Push that change to your GitHub repository.
4. Write the URL of your running Heroku app here: ``` http://cis411lab2-em1404.herokuapp.com/graphql```
5. Embed _using markdown_ a screenshot of your successful build and deployment to Heroku of your project.
![Build and deployment to Heroku](CircleCI_build.jpg)
6. Answer the questions below.
7. Submit a Pull Request to cis411_lab2 and provide the URL of that Pull Request in Canvas as your URL submission.

## Questions
1. Why would a containerized version of an application be beneficial if you can run the application locally already?

> * ``` Useful for applications portability to other machines```
> * ``` Applications are safer in containers because of isolation capabilities ```
> * ``` Simplifies continous intergration and continouos deployment of applications ```

2. If we have the ability to publish directory to Heroku, why involve a CI solution like CircleCI? What benefit does it provide?

> * ``` Runs the automated test scripts during integration and deployment. ```
> * ``` The developer gets notified via email when there is an error or that the build was successful, and the code has been pushed to the staging server for preview. ```