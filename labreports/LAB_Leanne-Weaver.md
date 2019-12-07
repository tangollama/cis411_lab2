# Lab Report Template for CIS411_Lab2
Course: Messiah College CIS 411, Fall 2019

Instructors: [Joel Worrall](https://github.com/tangollama) & [Trevor Bunch](https://github.com/trevordbunch)
Name: Leanne Weaver

GitHub: [Leanne-Weaver](https://github.com/Leanne-Weaver)

# Required Content

1. Generate a markdown file in the labreports directory named LAB_[GITHUB HANDLE].md. Write your lab report there. :heavy_check_mark:
2. Create the directory ```./circleci``` and the file ```.circleci/config.yml``` in your project and push that change to your GitHub repository. :heavy_check_mark:
3. Create the file ```Dockerfile``` in the root of your project and include the contents of the file as described in the instructions. Push that change to your GitHub repository. :heavy_check_mark:
4. Write the URL of your running Heroku app here: ```ex: http://[cis411lab2-leanne-weaver.herokuapp.com/graphql``` :heavy_check_mark:
5. Embed _using markdown_ a screenshot of your successful build and deployment to Heroku of your project. :heavy_check_mark:
[!GraphiQL Screenshot](../../GraphiQL_Screenshot.PNG)
[!Earliest builds in CircleCI](../CircleCI_Snippet1.PNG)
[!Latest builds in CircleCI](../CircleCi_Snippet2.PNG)
6. Answer the questions below. _(See below)_ :heavy_check_mark:
8. Submit a Pull Request to cis411_lab2 and provide the URL of that Pull Request in Canvas as your URL submission. :heavy_check_mark:

## Questions
1. Why would a containerized version of an application be beneficial if you can run the application locally already?<br>
Putting my application in a container will allow reliable and efficient transport of my application to other software environments. This will mitigate the headaches and errors that can be caused by slight discrepancies between the application's interactions with infrastructures of differing software environments.

2. If we have the ability to publish directory to Heroku, why involve a CI solution like CircleCI? What benefit does it provide?<br>
The main benefit provided by CircleCI is that it tests code committed to GitHub. Validated code will be pushed, but code that fails the tests and is deemed as buggy will be rejected. This can help us detect _where_ the breakdown occurs (by looking only at the files in the rejected commit), as well as preserve the integrity of the functionality of the code that is already pushed.
