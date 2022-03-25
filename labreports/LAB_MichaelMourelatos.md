# Lab Report: CD
___
**Course:** CIS 411, Spring 2022  
**Instructor(s):** [Trevor Bunch](https://github.com/trevordbunch)  
**Name:** Michael Mourelatos  
**GitHub Handle:** [MichaelMourelatos](https://github.com/MichaelMourelatos)  
**Repository:** [My Forked Repository](https://github.com/MichaelMourelatos/cis411_lab4_CD)  
**Collaborators:** [Grace Schlauder](https://github.com/grace-schl)
___

# Required Content

- [x] Generate a markdown file in the labreports directoy named LAB_[GITHUB HANDLE].md. Write your lab report there.
- [x] Create the directory ```./circleci``` and the file ```.circleci/config.yml``` in your project and push that change to your GitHub repository.
- [x] Create the file ```Dockerfile``` in the root of your project and include the contents of the file as described in the instructions. Push that change to your GitHub repository.
- [x] Embed _using markdown_ a screenshot of your successful build and deployment to Heroku of your project (with the circleci interface).  

**Successful Build**:
![Successful Build](/Successful_Build_and_Deployment.png)

**Recent Successful Build**:
![Recent Successful Build](/Successful_Build.png)


- [x] Write the URL of your running Heroku app here (and leave the deployment up so that I can test it):  


[URL for Heroku app with Graphql](http://cis411lab4-michaelmourelatos.herokuapp.com/graphql)

**Successful Build**:
![Image of HerokuGraphql](/Correct_Screeshot_Off_Heroku.png)


- [x] Answer the **4** questions below.
- [x] Submit a Pull Request to cis411_lab4_CD and provide the URL of that Pull Request in Canvas as your URL submission.

## Questions
1. Why would a containerized version of an application be beneficial if you can run the application locally already?
- A containerized version would be beneficial due to the application already having all of the necessary components and dependencies needed for an application to run smoothly. Another practical factor to containerized versions of applications would be that multiple team members would be able to run the application with different setups. So, having the containerized version will give various users the same view despite different setups. All of these factors play together to give an efficient user experience when working on a team.

2. If we have the ability to publish directory to Heroku, why involve a CI solution like CircleCI? What benefit does it provide?
- We are using CircleCi to ensure that the building processes are running smoothly and how they should be. CircleCi tells the users if the current build has failed or is successful, which is critical due to the code needing to be deployable. Publishing right to the directory of Heroku would skip over the process of CI/CD. Users should utilize the in-between step of CircleCi to ensure their code is successful and has a green light to continue moving forward.
3. Why would you use a container technology over a virtual machine(VM)?
- [Containers](https://www.backblaze.com/blog/vm-vs-containers/) require less of a setup and require fewer resources to operate compared to VMs. Meaning, containers are more time-efficient by not needing to utilize as many resources. Containers are light in size, take seconds to start, and can run multiple applications compared to VMs, which are large and take minutes to fire up.
4. What are some alternatives to Docker for containerized deployments?
- Some examples of alternatives to Docker would be:
  - [Podman](https://podman.io/)
  - [Kubernetes](https://kubernetes.io/)
  - [LXC](https://linuxcontainers.org/)
  - [Containerd](https://www.vagrantup.com/)

What I used to [reference](https://rigorousthemes.com/blog/best-docker-alternatives/) for my alternatives.