# Lab Report Template for CIS411_Lab2
Course: Messiah College CIS 411, Fall 2018

Instructors: [Joel Worrall](https://github.com/tangollama) & [Trevor Bunch](https://github.com/trevordbunch)

Name: Caleb Weaver

GitHub: [Cweaver136](https://github.com/Cweaver136)

# Required Content
URL of your running Heroku app: ```ex: https://cis411lab2-cweaver136.herokuapp.com/graphql```

Embed _using markdown_ a screenshot of your successful build and deployment to Heroku of your project.
    
![Command Terminal deploying the project](../assets/cmd_heroku.png "Terminal")
![Graphql view of our project](../assets/web_heroku.png "Graphql")

## Questions
1. Why would a containerized version of an application be beneficial if you can run the application locally already?


    > Using a container allows anybody from any machine to run your code. They don'y have to worry about setting up any config stuff, they can just run it straight up. While you can still run in locally, that's only on your machine. If you use a container, you can include other people in your testing and development more easily.

2. If we have the ability to publish directory to Heroku, why involve a CI solution like CircleCI? What benefit does it provide?

    > CircleCi allows us to detect any problems with our code before it even get to Heroku. It limits errors and help us write cleaner code.
