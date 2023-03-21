# Lab Report: UX/UI
___
**Course:** CIS 411, Spring 2021  
**Instructor(s):** [Trevor Bunch](https://github.com/trevordbunch)  
**Name:** Ray Truex <br>
**GitHub Handle:** rt1252 <br>
**Repository:** [Your Forked Repository](https://github.com/rt1252/cis411_lab4_CD/tree/purelab) <br>
**Collaborators:** NA
___

# Required Content

- [x] Generate a markdown file in the labreports directory named LAB_[GITHUB HANDLE].md. Write your lab report there.
- [x] Create the directory ```./circleci``` and the file ```.circleci/config.yml``` in your project and push that change to your GitHub repository.
- [x] Create the file ```Dockerfile``` in the root of your project and include the contents of the file as described in the instructions. Push that change to your GitHub repository.
- [x] Write the URL of your app hosted on Heroku or other Cloud Provider here:  
[https://lab4-lfanl.ondigitalocean.app/graphqll](https://lab4-lfanl.ondigitalocean.app/graphql)
- [x] Embed _using markdown_ a screenshot of your successful deployed application to Digital Ocean.  
> ![Successful Build](/assets/digital_ocean.png)
- [x] Embed _using markdown_ a screenshot of your successful build and deployment to Digital Ocean of your project (with the circleci interface).  
> Example: ![Successful Build](/assets/circleci2.png)
- [x] Answer the **4** questions below.
- [x] Submit a Pull Request to cis411_lab4_CD and provide the URL of that Pull Request in Canvas as your URL submission.

## Questions
1. Why would a containerized version of an application be beneficial if you can run the application locally already?
> Containers are much more beneficial than running applications locally, while running local may seem to be easier and save time it is almost always better to use containers. Containers provide many benefits, one of the biggest being portability, containers are a way of packaging an application and all of its dependencies into a single unit that can be easily moved across environments. By having the dependencies included in the container you can be sure that your application will run correctly no matter where it is deployed. Containers also allow for much greater scalability. 
2. If we have the ability to publish directory to Heroku, why involve a CI solution like CircleCI? What benefit does it provide?
> The two main reasons that involving a solution like CircleCI on top of Heroku is for automated testing and monitoring. CircleCI and CI pipelines can be set up to run automated tests every time a change is made to the codebase, this helps catch bugs. Secondly, monitoring tools can be integrated that allow you to see the metrics of your system. 
3. Why would you use a container technology over a virtual machine(VM)?
> There are many reasons to use containers over virtual machines. Containers package everything it needs to run the application into a very small container, virtual machines on the other hand are very large and need gigabytes to be stored. You can run more containers on a single host than if you were using VMs which can help reduce hardware costs. In addition, containers also use fewer resources than VMs do this also increases efficiency and reduces costs. Lastly containers are faster and can be started and stopped much faster than VMs.
4. What are some alternatives to Docker for containerized deployments?
> The main competitor for Docker that comes to mind for me is Kubernetes, Kubernetes is useful for deploying containers at scale. It provides many features such as managing containers, auto scaling containers, rolling updates, and load balancing. A more different competitor is Podman which is a daemonless open source Linux tool that makes running Docker more lightweight.
