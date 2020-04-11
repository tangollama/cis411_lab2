# Lab Report Template for CIS411_Lab2
Course: Messiah College CIS 411, Fall 2018

Instructors: [Joel Worrall](https://github.com/tangollama) & [Trevor Bunch](https://github.com/trevordbunch)

Name: Will Newcomb

GitHub: [Willnew98](https://github.com/Willne98)

# Required Content

1. Generate a markdown file in the labreports directoy named LAB_[GITHUB HANDLE].md. Write your lab report there.
2. Create the directory ```./circleci``` and the file ```.circleci/config.yml``` in your project and push that change to your GitHub repository.
3. Create the file ```Dockerfile``` in the root of your project and include the contents of the file as described in the instructions. Push that change to your GitHub repository.
4. Write the URL of your running Heroku app here: ```https://cis411lab2-willnew98.herokuapp.com/graphql```
5. Embed _using markdown_ a screenshot of your successful build and deployment to Heroku of your project.
6. Answer the questions below.
7. Submit a Pull Request to cis411_lab2 and provide the URL of that Pull Request in Canvas as your URL submission.

## Questions
1. Why would a containerized version of an application be beneficial if you can run the application locally already?
* The biggest benefit to having a containerized version of an application is to ease the process of testing. Running the application locally to test can get cluttered and hectic. With Docker, you're able to containerize everything and build more complex applications. Docker also allows the ability to easily fix anything you might have broken, no matter how big.
2. If we have the ability to publish directory to Heroku, why involve a CI solution like CircleCI? What benefit does it provide?
* Heroku has made deployment so much easier for developers. But, CircleCI or some other continuous integration is needed. This allows for easy deployment, and then that code is put through the CircleCI delivery pipeline. All of the tests will run, and only if it passes, will it then be pushed to Heroku. CircleCI acts almost like a fact checker before going to Heroku with possibly buggy code.
