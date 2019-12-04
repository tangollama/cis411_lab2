1. # Lab Report Template for CIS411_Lab2

    

   Course: Messiah College CIS 411, Fall 2018

    

   Instructors: [Joel Worrall](https://github.com/tangollama) & [Trevor Bunch](https://github.com/trevordbunch)

    

   Name: Drew Feldman

    

   GitHub: [DrewRFeldman](https://github.com/drewrfeldman)

    

   # Required Content

    

   1. Generate a markdown file in the labreports directoy named LAB_[GITHUB HANDLE].md. Write your lab report there.
   
   2. Create the directory `./circleci` and the file `.circleci/config.yml` in your project and push that change to your GitHub repository.
   
   3. Create the file `Dockerfile` in the root of your project and include the contents of the file as described in the instructions. Push that change to your GitHub repository.
   
   4. Write the URL of your running Heroku app here: `ex: https://cis411lab2-drewrfeldman.herokuapp.com/graphQL`

   5. Embed *using markdown* a screenshot of your successful build and deployment to Heroku of your project.

      Terminal Success

      ![Capture]https://github.com/DrewRFeldman/cis411_lab2/tree/master/labreports/capture.png

      CircleCI Success (after many attempts)
   
      ![Capture]https://github.com/DrewRFeldman/cis411_lab2/tree/master/labreports/capture2.png
   
   6. Answer the questions below.
   
   7. Submit a Pull Request to cis411_lab2 and provide the URL of that Pull Request in Canvas as your URL submission.
   
    
   
   ## Questions
   
    
   
   1. Why would a containerized version of an application be beneficial if you can run the application locally already?
   
      I think the benefit of this containerized application is that it can be run from other systems by simply connecting to the url, allowing a larger number of testers more conveniently. Alternatively, my computer has almost no memory and pushing this process to an external processor helps my computer to survive.
   
      It also causes all instances of the code to be run in the same environment, regardless of operating system or hardware. This creates consistency between users which may aid in development as well as debugging.
   
   2. If we have the ability to publish directory to Heroku, why involve a CI solution like CircleCI? What benefit does it provide?
   
      CircleCI allows us to detect errors as soon as we push. Like I saw with my eight separate pushes to get Heroku working, it detects problems immediately before they ever make it to heroku. This aids in error remediation.