Course: Messiah College CIS 411, Spring 2020<br/>
Instructors: [Trevor Bunch](https://github.com/trevordbunch)<br/>
Name: Matthew Coates<br/>
GitHub: [slycatm2](https://github.com/slycatm2)<br/>
Heroku App: https://cis411lab2-slycatm2.herokuapp.com/graphql<br/>
1. Why would a containerized version of an application be 
beneficial if you can run the application locally already?
Containerized versions can use memory, CPU usage and storage more efficiently 
than running an application locally. Contrainerized software will also always
run the same regardless of the infrastructure used, which can't be said of 
local apps. Lastly, it allows businesses to launch individual applications
without the need to rent an entire VM.<br/>

2. If we have the ability to publish directly to Heroku, 
why involve a CI solution like CircleCI? What benefit does it provide?
It shows whether or not your master pushes were successfully pushed to git or not. <br/>

* A screenshot of the _Jobs_ list in CircleCI
![](2020-04-19-12-09-41.png)

* A screenshot of the heroku app working. 
![](2020-04-19-12-09-06.png)