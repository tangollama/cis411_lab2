# Lab Report Template for CIS411_Lab2

Course: Messiah College CIS 411, Fall 2018

Instructors: [Joel Worrall](https://github.com/tangollama) & [Trevor Bunch](https://github.com/trevordbunch)

Name: Joshua Keong Wei Xian

GitHub: [jk1595](https://github.com/jk1595)

# Required Content

1. Generate a markdown file in the labreports directoy named LAB\_[GITHUB HANDLE].md. Write your lab report there.
2. Create the directory `./circleci` and the file `.circleci/config.yml` in your project and push that change to your GitHub repository.
3. Create the file `Dockerfile` in the root of your project and include the contents of the file as described in the instructions. Push that change to your GitHub repository.
4. Write the URL of your running Heroku app here: `http://cis411lab2-jk1595.herokuapp.com/graphql`
5. Embed _using markdown_ a screenshot of your successful build and deployment to Heroku of your project.
   ![SuccessfulBuild](../assets/SuccessfulBuild.png "SuccessfulBuild")

6. Answer the questions below.
7. Submit a Pull Request to cis411_lab2 and provide the URL of that Pull Request in Canvas as your URL submission.

## Questions

1. Why would a containerized version of an application be beneficial if you can run the application locally already?

   Dependencies or settings within a container will not affect any configurations on your computer, or on any other containers that may be running. Also, by using separate containers for each component of an application, you can avoid conflicting dependencies. Using containers will also provide better security; if one container is compromised the others would not be affected.

2. If we have the ability to publish directory to Heroku, why involve a CI solution like CircleCI? What benefit does it provide?

   CircleCI will collect all the code and its changes in one place, prepares it to be published, and tests the code release. This help remove any human error in code review, it saves the team time and increases the quality of the code.
