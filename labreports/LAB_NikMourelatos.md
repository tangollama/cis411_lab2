# Lab Report Template for CIS411_Lab2
Course: Messiah College CIS 411, Fall 2018

Instructors: [Joel Worrall](https://github.com/tangollama) & [Trevor Bunch](https://github.com/trevordbunch)

Name: Nik Mourelatos

GitHub: [NikMourelatos](https://github.com/NikMourelatos)

# Required Content

1. Generate a markdown file in the labreports directoy named LAB_[GITHUB HANDLE].md. Write your lab report there.
2. Create the directory ```./circleci``` and the file ```.circleci/config.yml``` in your project and push that change to your GitHub repository.
3. Create the file ```Dockerfile``` in the root of your project and include the contents of the file as described in the instructions. Push that change to your GitHub repository.
4. Write the URL of your running Heroku app here: ```ex: https://cis411lab2-nikmourelatos.herokuapp.com/graphql```
5. Embed _using markdown_ a screenshot of your successful build and deployment to Heroku of your project.

[Heroku Deployment](images/Deployment.jpg)

6. Answer the questions below.
7. Submit a Pull Request to cis411_lab2 and provide the URL of that Pull Request in Canvas as your URL submission.

## Questions
1. Why would a containerized version of an application be beneficial if you can run the application locally already?

Containarized version of apps provide a smoother and more efficient deployment, allowing for all DevOps members to view  their own  application regardless of the computer/Operating System they have.   

Altogether, using a container allows the DevOps team to control the dependencies of an application, have greater efficiency and consistency in deployment, all while increasing the portability of the application as, in a container, it can be ran from an OS.

2. If we have the ability to publish directory to Heroku, why involve a CI solution like CircleCI? What benefit does it provide?

CircleCi is used for continuous integration, meaning all members of DevOps publish their code to CircleCI prior to it  going to continous deployment in Heroku. By doing this CircleCi is able to run tests on the published code making sure that it  is error free and deployed correctly to our Heroku container.  With continuous integration in place we are also able to commit code more often all while having a smaller backlog.

