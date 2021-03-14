# CIS 411 Lab 4: Continuous Deployment
This is the Continuous Deployment (CD) Lab for CIS 411: Systems Analysis and Design for [Messiah University](http://messiah.edu)

The purpose of this lab is to get hands on experience working with Docker, CircleCI, and a Cloud Service Provider like Heroku to create a CI/CD pipeline. Though the lab is generally paint by numbers, the hands on experience with the tools is meant to prepare students to improvise on this relatively simple implementation as teams approach CIS 471/472.  

# Doing the Lab

## 1. Pre-Requisites
1. GitHub account
2. Git is installed on your development machine.
3. Text editor or other integrated development environment (IDE) for modifying code.  
...
4. You will install Docker (and need an account on Docker Hub) as part of this lab.
5. You will install Heroku CLI (and setup a free account) as part of this lab.

## 2. Lab Description
This lab will build upon your prior experience using CircleCI in [lab 1](https://github.com/trevordbunch/cis411_lab1_CI) for the first two steps.  Step 3 will packaging the GraphQL application into a Docker container.  Step 4 will focus on setting up the Heroku deployment location, and Step 5 will guide you through setting up the CI/CD pipeline in CircleCI.  After the lab, you will need to respond to 4 questions about why container technology is useful in modern architectures.

Detailed instructions are [here](LAB_INSTRUCTIONS.md), and you are expected to compile your findings into a labreport following this [template](labreports/LAB_TEMPLATE.md).

## 3. Submissions
You are expected to create a lab report as a markdown file under the labreports directory using the **LAB_[GITHUB Handle].md** naming convention in your forked repository.  After you have reviewed your work, then you should submit a `Pull Request` to this repository with your lab report and any accompanying images/files (e.g., required diagrams).  Add the `Pull Request` URL into the courseroom LMS (Canvas) for grading.

# Resources
Lab Specific Help.
- [Detailed instructions](LAB_INSTRUCTIONS.md)
- [Lab template](labreports/LAB_Template.md)
- [HELP: Installing Docker on a Windows Home edition laptop](ex/Docker_Installation_Win10_Home.md)

Understanding Markdown Syntax
- [Markdown Guide](https://www.markdownguide.org/)
- [Github Flavored Markdown](https://github.github.com/gfm/)
- [Table to Markdown tool](https://tabletomarkdown.com/convert-spreadsheet-to-markdown/)
  
CircleCI Resources
- [Configuration Components](https://circleci.com/docs/2.0/concepts/?section=getting-started#configuration)
- [CircleCI Pre-configured Packages (aka Orbs)](https://circleci.com/docs/2.0/using-orbs/)

Docker Resources
- [Docker Installation](https://docs.docker.com/get-docker/)
- [Docker Hub Accounts](https://hub.docker.com/)

Heroku Resources
- [Heroku Account](https://signup.heroku.com)
- [Heroku CLI Download](https://devcenter.heroku.com/articles/heroku-cli#download-and-install)

# License
This content is provided under the `MIT` [license](LICENSE).

# Credits
Special thanks to Joel Worrall, aka [tangollama](https://github.com/tangollama), for co-developing this course and writing this lab.

[Tanner Stern](https://github.com/tannerstern/) compiled a tutorial on how to install Docker on Windows Home Edition [(here)](https://tabletomarkdown.com/convert-spreadsheet-to-markdown/) and added the associated windows bat files.