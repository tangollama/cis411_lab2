# Lab Report Template for CIS411_Lab2
Course: Messiah College CIS 411, Fall 2018

Instructors: [Joel Worrall](https://github.com/tangollama) & [Trevor Bunch](https://github.com/trevordbunch)

Name: Andrew Douglass

GitHub: [douglassjohnandrew](https://github.com/douglassjohnandrew)

# Required Content

1. Generate a markdown file in the labreports directory named LAB_[GITHUB HANDLE].md. Write your lab report there.
2. Create the directory ```./circleci``` and the file ```.circleci/config.yml``` in your project and push that change to your GitHub repository.
3. Create the file ```Dockerfile``` in the root of your project and include the contents of the file as described in the instructions. Push that change to your GitHub repository.
4. Write the URL of your running Heroku app here: https://cis411lab2-douglassjohnandrew.herokuapp.com/graphql
5. Embed _using markdown_ a screenshot of your successful build and deployment to Heroku of your project.
![CircleCI](/screenshots/CircleCI_success.png?raw=true)
![Heroku](/screenshots/Heroku_success.png?raw=true)

6. Answer the questions below.
7. Submit a Pull Request to cis411_lab2 and provide the URL of that Pull Request in Canvas as your URL submission.

## Questions
1. Why would a containerized version of an application be beneficial if you can run the application locally already?<br/></br>
Containers are much more lightweight than virtual machines and are highly scalable. Containerized versions of applications are also more easily shareable and efficient than traditional virtual machines. In addition, using containers places further emphasis on cloud-native development, and fosters functionality across operating systems. [Source used](http://www.monitis.com/blog/top-5-benefits-of-containerization/)<br/><br/>
2. If we have the ability to publish directory to Heroku, why involve a CI solution like CircleCI? What benefit does it provide?<br/><br/>
Whereas Heroku allows developers to check the status of their application at any given time, CircleCI specializes in continuous integration, or repeatedly making many small, frequent changes. CircleCI excels at letting developers know when a change they push causes the app to malfunctio by checking dependencies, testing, and deployment. In this way, CircleCI provides some benefits that Heroku cannot provide, and vice versa. [Source used](https://circleci.com/blog/what-is-continuous-integration/)
