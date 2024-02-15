Jenkinsfile

As of now we have seen that the configuration of a Job we have done in the UI of Jenkins.
Same thing we can do by writing the code and storing the code into a File named Jenkinsfile

So we can write Pipeline as a Code. We store Jenkinsfile in the Repository with the code.

Lets create a JOB

![image](https://github.com/devops-pritam/jenkins/assets/132892500/16e95982-60e5-4b2c-9b5d-4bdc86a23753)

Select Pipeline Job

![image](https://github.com/devops-pritam/jenkins/assets/132892500/3a16490a-1dc9-4813-a33b-af1f8b0890c2)

Here we can write the Script in the Jenkins Console

![image](https://github.com/devops-pritam/jenkins/assets/132892500/74242700-8b10-4d7b-9f74-7b6d18af1295)

Or else we can use a file stored inside out git repo

![image](https://github.com/devops-pritam/jenkins/assets/132892500/dcd3b228-ee2d-4b78-bdfd-9b79a3c7a868)

First lets write the Pipeline code as we have done earlier
![image](https://github.com/devops-pritam/jenkins/assets/132892500/a10138c2-b1c1-4b18-b4c3-4a4f3d0b3db0)

pipeline {
    agent any

    stages {
        stage('parameter') {
            steps {
                script {
                
                properties([parameters([choice(choices: ['yes', 'no'], name: 'shouldWePrint')])])
                        }
                  }
            
        
        }
        stage('Print') {
            when {
                expression { 
                   return params.shouldWePrint == 'yes'
                }
            }
            steps {
                    sh """
                    java --version
                    """
                }
            }
        stage('No Print') {
            when {
                expression { 
                   return params.shouldWePrint == 'no'
                }
            }
            steps {
                    echo 'No Print Required'
                }
            }
   }
        
    
}

Lets test it First

Apply + Save

![image](https://github.com/devops-pritam/jenkins/assets/132892500/2435a2b6-827e-4529-8a97-84c72330c60e)

Build with Parameter
![image](https://github.com/devops-pritam/jenkins/assets/132892500/e18b19c1-8dc5-4881-8e29-55a7ef7b67ef)
Parameter as yes and build it
![image](https://github.com/devops-pritam/jenkins/assets/132892500/e9af393d-18a0-41a3-aaef-fe1985785f56)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/f697de46-18e7-49fd-bc78-14c8fc2ce974)

Now lets copy the same code and paste it to the Jenkinsfile
![image](https://github.com/devops-pritam/jenkins/assets/132892500/d1091844-9dfe-4582-8610-65bfd1d852ea)

now, lets select the code from SCM and give the repo details

![image](https://github.com/devops-pritam/jenkins/assets/132892500/d943eb31-64b2-4519-9375-8c60a25866b8)
![image](https://github.com/devops-pritam/jenkins/assets/132892500/4d6032f7-2dc7-4379-9969-1f831daef4e2)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/e05f25ec-9784-4b8c-a289-7ba82154d9bb)

Apply + save 

![image](https://github.com/devops-pritam/jenkins/assets/132892500/b082bdef-1197-47a7-bd9c-4a6175557189)

Build with Parameter

![image](https://github.com/devops-pritam/jenkins/assets/132892500/ae6483bf-48c1-402a-9147-1a4b18e81d8d)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/1f805e71-4a97-4086-b7c7-2821d794ea09)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/b2ad3f19-5101-4dd5-a39d-30d67e56d35d)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/c6e153e7-6064-4f25-89dd-dd95234a7cae)

Now, lets go to the Jenkins UI and select Pipeline Script
![image](https://github.com/devops-pritam/jenkins/assets/132892500/fb445535-071d-4bf0-8615-6fdc8863e559)

Use the Hello World Sample

Here, we are going to clone the Git Repo using the Code, For that click on the Pipeline Syntax

![image](https://github.com/devops-pritam/jenkins/assets/132892500/a023fa0f-caea-4f4c-968b-a284544cf1a7)

Select Git from the Dropdown
![image](https://github.com/devops-pritam/jenkins/assets/132892500/99924dd7-a294-4734-b29a-4250d2868983)

Give URL of the repo and the Branch name
![image](https://github.com/devops-pritam/jenkins/assets/132892500/78ac6751-8b3b-4209-820a-e9a80a99de99)

Then click on Generate Pipeline Script

![image](https://github.com/devops-pritam/jenkins/assets/132892500/f4785db5-6292-44f4-a4a1-b862d01493c6)

Copy the Code
![image](https://github.com/devops-pritam/jenkins/assets/132892500/d7216e8e-0c8a-442f-8a87-64d48f64b158)

And us ethe same like this 
![image](https://github.com/devops-pritam/jenkins/assets/132892500/1a998265-16b5-46b9-b762-6dd4951f3b3c)

Apply + Save 
![image](https://github.com/devops-pritam/jenkins/assets/132892500/2c8f5f8e-1bfa-4d06-ba41-42cc83ccef79)

Then Build Now
![image](https://github.com/devops-pritam/jenkins/assets/132892500/337f9ec5-d9cf-4cc5-97de-a2f0971026a5)

If we are getting this kind of issue

![image](https://github.com/devops-pritam/jenkins/assets/132892500/db3fc2d7-0f15-4954-bbd5-1b555dba1ae3)

Problem here was that the workflow-aggregator:2.6 has a dependency on git-client plugin. Plugin 'git' was installed manually after the jenkins was booted up with workflow-aggregator and the server was never restarted after manual installation of git.

So, pipeilne assumed the usage git-client instead of git plugin. After the jenkins was restarted, the git plugin worked and above mentioned step to checkout worked.

So lets restart the jenkins server

![image](https://github.com/devops-pritam/jenkins/assets/132892500/a7616cd1-ecb5-463c-bf0c-370b35a928af)

Then Build the Job again

![image](https://github.com/devops-pritam/jenkins/assets/132892500/a82fdcb6-bcd8-4e6e-b297-a55883dad885)
































