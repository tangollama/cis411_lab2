# Lab Report Template for CIS411_Lab2
Course: Messiah College CIS 411, Fall 2018

Instructors: [Joel Worrall](https://github.com/tangollama) & [Trevor Bunch](https://github.com/trevordbunch)

Name: Samuel Mahan

GitHub: [SamMahan](https://github.com/SamMahan)

# Required Content

1. Generate a markdown file in the labreports directoy named LAB_[GITHUB HANDLE].md. Write your lab report there.
2. Create the directory ```./circleci``` and the file ```.circleci/config.yml``` in your project and push that change to your GitHub repository.
3. Create the file ```Dockerfile``` in the root of your project and include the contents of the file as described in the instructions. Push that change to your GitHub repository.
4. Write the URL of your running Heroku app here: ```ex: https://cis411lab2-sammahan.herokuapp.com/graphql```
5. Embed _using markdown_ a screenshot of your successful build and deployment to Heroku of your project.
{My Successful Build}{https://github.com/SamMahan/cis411_lab2/blob/master/labreports/Capture.JPG}
6. Answer the questions below.
7. Submit a Pull Request to cis411_lab2 and provide the URL of that Pull Request in Canvas as your URL submission.

## Questions
1. Why would a containerized version of an application be beneficial if you can run the application locally already?
-I want to ensure that my local environment is identical to those of the developers I work with to avoid a scenario where the code works for some people and not for others due to inconsistent environments. 
2. If we have the ability to publish directory to Heroku, why involve a CI solution like CircleCI? What benefit does it provide?
CircleCI performs tests that allow us to validate the code before it is pushed. It acts as an automatic gatekeeper that will turn away commits that cause errors or fail tests. This way, we can guarantee that our new commits never break older functionality.
