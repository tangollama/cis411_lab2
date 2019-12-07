1. # Lab Report Template for CIS411_Lab2

    

   Course: Messiah College CIS 411, Fall 2018

    

   Instructors: [Joel Worrall](https://github.com/tangollama) & [Trevor Bunch](https://github.com/trevordbunch)

    

   Name: Stephen Maloney

    

   GitHub: [sm1535](https://github.com/sm1535)

    

   # Required Content

    

   1. Generate a markdown file in the lab reports directory named LAB_[GITHUB HANDLE].md. Write your lab report there.
   
   2. Create the directory `./circleci` and the file `.circleci/config.yml` in your project and push that change to your GitHub repository.
   
   3. Create the file `Dockerfile` in the root of your project and include the contents of the file as described in the instructions. Push that change to your GitHub repository.
   
   4. Write the URL of your running Heroku app here: `ex: https://cis411lab2-sm1535.herokuapp.com/graphQL`

   5. Embed *using markdown* a screenshot of your successful build and deployment to Heroku of your project.

      ![Capture]https://github.com/sm1535/cis411_lab2/tree/master/labreports/Capture.PNG

      ![Capture]https://github.com/sm1535/cis411_lab2/tree/master/labreports/Capture2.PNG

   6. Answer the questions below.
   
   7. Submit a Pull Request to cis411_lab2 and provide the URL of that Pull Request in Canvas as your URL submission.
   
    
   
   ## Questions
   
    
   
   1. Why would a containerized version of an application be beneficial if you can run the application locally already?
   
      Containerized applications allow developers to run the program in the same environment regardless of the hardware and software of the developers, creating a form of consistency among the team.
   
      
   
   2. If we have the ability to publish directory to Heroku, why involve a CI solution like CircleCI? What benefit does it provide?
   
      CircleCI lets us detect errors before they ever make it to heroku. This is really convenient for catching errors in your code or even errors in other member's pushes before issues are able to compound and cause bigger problems. 
