Setup Jenkins Pipeline and run the job 

Click on Manage Jenkins
![image](https://github.com/devops-pritam/jenkins/assets/132892500/e5f68bdb-10c2-4af9-87a6-eb5384d1311f)

Click on Plugins

![image](https://github.com/devops-pritam/jenkins/assets/132892500/db2f1850-dd4e-41d4-9906-2a77c48c6426)

Select the Pipeline Plugins

![image](https://github.com/devops-pritam/jenkins/assets/132892500/c51b8b9b-6582-4945-94ad-8fb3ad47122c)

Click on Install

![image](https://github.com/devops-pritam/jenkins/assets/132892500/5dd532d9-69d1-470a-922d-c560f7384229)

Once everything is installed 

![image](https://github.com/devops-pritam/jenkins/assets/132892500/6b779e02-b73b-4313-8cde-6badec1c796a)

Go back to dashboard and Create New Item

![image](https://github.com/devops-pritam/jenkins/assets/132892500/063462d6-3b03-48ff-b0c0-08bfaaea86cb)

Select Pipeline and create a New Pipeline

![image](https://github.com/devops-pritam/jenkins/assets/132892500/824ae586-8165-48e6-9308-d4b648f13c6b)

Lets Go to Pipeline

![image](https://github.com/devops-pritam/jenkins/assets/132892500/71c6699b-048a-421e-8e2c-ad1b97e783b7)

Here we are basically saying we are going to write some code to achieve something

Select the Hellow World Project

![image](https://github.com/devops-pritam/jenkins/assets/132892500/219b08b2-a7bb-4e0c-b27f-68ed3b079fd0)

And we can see this code automatically

![image](https://github.com/devops-pritam/jenkins/assets/132892500/87d9d992-4f59-4180-ba17-6c2f07e877fe)

This is a declarative pipeline, which starts with pipeline syntax

agent any , means the code can run anywhere / any system, And it does not need any special pre configured systems to run the code

![image](https://github.com/devops-pritam/jenkins/assets/132892500/f5fae838-294f-4a26-83d8-c1c890c3dc4c)

Then we have stages , means what are the activities we are going to achieve from this pipeline. And under the stages we can have many stage and under the stage we can have steps.

![image](https://github.com/devops-pritam/jenkins/assets/132892500/7a9712d9-a71f-42ea-85cf-ee3213863773)

Apply and SAVE
![image](https://github.com/devops-pritam/jenkins/assets/132892500/939f9be0-f93b-4894-a60d-96ebc6bf13d6)

Lets Build the project

![image](https://github.com/devops-pritam/jenkins/assets/132892500/d7f3bc44-95fd-406d-88ee-c4d6c90b457b)

Build is running

![image](https://github.com/devops-pritam/jenkins/assets/132892500/b2470033-09ff-4339-abd8-fccef0bfa10d)

Build is Successful

![image](https://github.com/devops-pritam/jenkins/assets/132892500/c77f3468-b787-41af-8bdd-a9ca1ce424c0)

In console Output we can see this result

![image](https://github.com/devops-pritam/jenkins/assets/132892500/a6781ec8-21de-4616-8aec-d9facd352b39)


Now, lets install the Stage View Plugin

![image](https://github.com/devops-pritam/jenkins/assets/132892500/a243aef8-abfe-4ab2-b20d-82ea3fe89b3e)

As soon as we install this plugin we can see the output like this

![image](https://github.com/devops-pritam/jenkins/assets/132892500/102e9b1b-7ca1-400e-870d-16ad1339b049)

And we can see the logs by this
![image](https://github.com/devops-pritam/jenkins/assets/132892500/b06ca2e7-687d-47cc-9413-968407499d20)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/1feeb29e-6748-4e84-b3fd-fa45782f6b85)






















