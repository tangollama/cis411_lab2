# Lab Report for CIS 411 Lab 2
Course: Messiah College CIS 411, Fall 2018

Instructors: [Joel Worrall](https://github.com/tangollama) & [Trevor Bunch](https://github.com/trevordbunch)

Name: Justin Kim

GitHub: [TymeOfNight](https://github.com/TymeOfNight)

# Required Content

Link to Heroku app: ```https://cis411lab2-tymeofnight.herokuapp.com/graphql```

Screenshot of successful deployment: ![Deployment on CircleCI](https://github.com/TymeOfNight/cis411_lab2/blob/master/assets/SuccessfulDeployment.png)

## Questions

1. Why would a containerized version of an application be beneficial if you can run the application locally already?

    ```Running the app in a predictable container eliminates development conflicts caused by conflicting configuration files.  It allows all members of a team to develop on identical (virtual) machines, even if their physical machines are different.```

2. If we have the ability to publish directory to Heroku, why involve a CI solution like CircleCI? What benefit does it provide?

    ```Involving CircleCI allows us to monitor building and heroku deployment, letting us know if something went wrong.  As a side benefit, you can have CircleCI run unit tests during the build process, maintaining code quality.```
