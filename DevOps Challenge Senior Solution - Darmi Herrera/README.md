# This is DevOps Challenge Senior Solution by Darmi Herrera Gutierrez.

**Architecture diagram demonstrating planned solution in AWS**
![](https://github.com/darmy14/timeoff-management-application-1/blob/master/DevOps%20Challenge%20Senior%20Solution%20-%20Darmi%20Herrera/Images/awsDiagram.PNG?raw=true)

**timeoff-management fork on local repository**
* https://github.com/darmy14/timeoff-management-application.git

**Required infrastructure running on cloud provider of preference, provisioned using some sort of
infrastructure as code solution.**
* In this section I used aws cloudformation, please check "awsCloudFormationTimeoff-management.json" file.
![](https://github.com/darmy14/timeoff-management-application-1/blob/master/DevOps%20Challenge%20Senior%20Solution%20-%20Darmi%20Herrera/Images/cloudformation.PNG?raw=true)
![](https://github.com/darmy14/timeoff-management-application-1/blob/master/DevOps%20Challenge%20Senior%20Solution%20-%20Darmi%20Herrera/Images/cloudformationStack.PNG?raw=true)

**Application must be deployed using a fully automated continuous integration solution, triggered by a change in source control.**
* In this section I used a Jenkins pipeline, triggered by a change in source control after 20 min since the change, this is a custom variable, 
  please check “jenkinsfile-timeoffmanagement.groovy” file.
![](https://github.com/darmy14/timeoff-management-application-1/blob/master/DevOps%20Challenge%20Senior%20Solution%20-%20Darmi%20Herrera/Images/jenkins.PNG?raw=true)

This is a Docker image pushed to the aws repo.

![](https://github.com/darmy14/timeoff-management-application-1/blob/master/DevOps%20Challenge%20Senior%20Solution%20-%20Darmi%20Herrera/Images/ECSimage.PNG?raw=true)

This is the web app running with all aws services created whit aws cloudformation file.

http://timeo-goril-1p23q03i5a20t-1992500154.us-east-1.elb.amazonaws.com/login/ 

![](https://github.com/darmy14/timeoff-management-application-1/blob/master/DevOps%20Challenge%20Senior%20Solution%20-%20Darmi%20Herrera/Images/timeoff-onAWS.PNG?raw=true)

**The application should be highly available, and load balanced.**

This section was provided by the architecture diagram, the awsCloudFormationTimeoffmanagement.jason and aws services created:

![](https://github.com/darmy14/timeoff-management-application-1/blob/master/DevOps%20Challenge%20Senior%20Solution%20-%20Darmi%20Herrera/Images/HAandLB.PNG?raw=true)

**Notes:**
* 1 . The Dokerfile in the time-off repository had to be modified because some libraries were missing.

![](https://github.com/darmy14/timeoff-management-application-1/blob/master/DevOps%20Challenge%20Senior%20Solution%20-%20Darmi%20Herrera/Images/Before.PNG?raw=true)

![](https://github.com/darmy14/timeoff-management-application-1/blob/master/DevOps%20Challenge%20Senior%20Solution%20-%20Darmi%20Herrera/Images/Now.PNG?raw=true)

* 2 . I really appreciate this opportunity, I hope that you understand that I don’t have too much time
cause my current job, so the Script for creating a new revision of a task definition and update an
aws service(cpu, ram, etc) is missing, I hope finish it and send it soon.
All the others code changes in the app are contemplated by the pipeline, and they will create a new image version.

