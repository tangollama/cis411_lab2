# Lab Report Template for CIS411_Lab2

Course: Messiah College CIS 411, Fall 2018

Instructors: [Joel Worrall](https://github.com/tangollama) & [Trevor Bunch](https://github.com/trevordbunch)

Name: Ethan Wong

GitHub: [ethanwwm](https://github.com/ethanwwm)

# Required Content

1. Generate a markdown file in the labreports directoy named LAB\_[GITHUB HANDLE].md. Write your lab report there.

2. Create the directory `./circleci` and the file `.circleci/config.yml` in your project and push that change to your GitHub repository.

3. Create the file `Dockerfile` in the root of your project and include the contents of the file as described in the instructions. Push that change to your GitHub repository.

4. Write the URL of your running Heroku app here: `http://cis411lab2-ethanwwm.herokuapp.com/graphql`

5. Embed _using markdown_ a screenshot of your successful build and deployment to Heroku of your project.

![Successful Heroku deployment](https://lh3.googleusercontent.com/cxM407omnJriXI11kvx9BOjxKLa8lUX1HnLQyuunDpN7Z7jRuwvcD3_3NcXOPDjVPmJq-iH32yv1YQ)

![Successful CircleCI test even though it failed](https://lh3.googleusercontent.com/rFqBN9satIZHqJ6uA04tnIBEtZVdtL7rB-MmsICox7V2spZI9oeCXrUYlS2ycMuoafJoLJDCjHF9qA)

6. Answer the questions below.

7. Submit a Pull Request to cis411_lab2 and provide the URL of that Pull Request in Canvas as your URL submission.

## Questions

1. Why would a containerized version of an application be beneficial if you can run the application locally already?

- A container can be beneficial in isolating the processes from seeing external processes outside the container. A container is also very fast because it shares the same kernel as the host system.

2. If we have the ability to publish directory to Heroku, why involve a CI solution like CircleCI? What benefit does it provide?

- CircleCI provides a seamless way of testing before deploying.
