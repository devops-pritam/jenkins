Create Jenkins Agent 


First Install this agent

![image](https://github.com/devops-pritam/jenkins/assets/132892500/e1e9520f-48aa-4c5b-9a72-b35449152d95)

Navigate to Jenkins Dashboard 

![image](https://github.com/devops-pritam/jenkins/assets/132892500/8d823cc8-9d87-4fb1-89e3-9725d25c3b2c)

Click on Manage Jenkins

Then Click on Node 

![image](https://github.com/devops-pritam/jenkins/assets/132892500/9b15efc5-6d52-4571-a3a3-eab362039a91)

Here we can click on New Node

![image](https://github.com/devops-pritam/jenkins/assets/132892500/4531c4e8-d9d9-4a96-a982-c87b459f94ea)

But there is another way of adding a New Node

In The Jenkins Dashboard click on Build Execution Status

![image](https://github.com/devops-pritam/jenkins/assets/132892500/e6c532d7-5a89-4f0f-b0ae-4e9e17b934ea)

Here we can click on New Node

![image](https://github.com/devops-pritam/jenkins/assets/132892500/1df0aa2d-067d-413d-80fe-2ba93734096c)

Lets Create ANother EC2 with Ubuntu OS

![image](https://github.com/devops-pritam/jenkins/assets/132892500/b609e4a5-af67-4ee9-aee4-39713af42582)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/9978cb63-b82d-4f35-bc16-fd824db48771)

Connect with the system

![image](https://github.com/devops-pritam/jenkins/assets/132892500/123ec476-105f-4fee-8eab-5e107798b863)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/a99a3f7e-92de-4388-9947-275e5dea25ce)

Install Java

![image](https://github.com/devops-pritam/jenkins/assets/132892500/93df22ff-535e-485b-8d79-32f67be818a3)

Check Java Version

![image](https://github.com/devops-pritam/jenkins/assets/132892500/f91c90ad-e03b-44e0-b514-d7f16fad837b)

Create a Directory called Jenkins using ubuntu user
![image](https://github.com/devops-pritam/jenkins/assets/132892500/60c1796a-f5cb-4ad9-b6f3-bc01546792b4)



Give full permission inside this directory

![image](https://github.com/devops-pritam/jenkins/assets/132892500/9b1a2a87-191a-4e01-a561-bd2d32540287)

Get the Path of this Directory

![image](https://github.com/devops-pritam/jenkins/assets/132892500/98306d12-b6a2-426f-8d23-48f0c96de30a)


Create A New Node 

![image](https://github.com/devops-pritam/jenkins/assets/132892500/f90e4495-b96d-450f-bf65-0e59582b3a74)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/3f0d5ef9-4954-4fff-8309-9bf1caf8eefe)

Click on Create

![image](https://github.com/devops-pritam/jenkins/assets/132892500/4b46f8f3-cbcc-43bd-90db-382e5fe9a70b)

Give name and description

![image](https://github.com/devops-pritam/jenkins/assets/132892500/c9f6a349-554d-47e2-98d7-26c9c836c377)

Lets Take No of Executer 2

![image](https://github.com/devops-pritam/jenkins/assets/132892500/bcb3c1ef-198c-4364-819c-762044a227e5)

No of Executor means 
![image](https://github.com/devops-pritam/jenkins/assets/132892500/dc40efc3-dc90-419f-b522-f8432d665bd4)

Give the directory Location of the server where we have created jenkins directory

![image](https://github.com/devops-pritam/jenkins/assets/132892500/01448ca7-89b4-4457-a8a9-24d28ad8d844)

Give the slave lable 
![image](https://github.com/devops-pritam/jenkins/assets/132892500/4b0b539c-db25-4032-bd61-daab9458e687)

We are going to use this slave as much as possible

![image](https://github.com/devops-pritam/jenkins/assets/132892500/50e4d311-9b39-401e-8930-4bae5f627bf2)

Launch Agent via SSH

![image](https://github.com/devops-pritam/jenkins/assets/132892500/87be7f2e-ad32-4184-b844-ad14ff9f2901)

Host is the Public IP of the server

![image](https://github.com/devops-pritam/jenkins/assets/132892500/a463bf75-a0ee-4aeb-bb27-0ad24fea6421)

Add credentials

![image](https://github.com/devops-pritam/jenkins/assets/132892500/3aa12d8f-2e25-4f3c-95e4-9bc065cf5be6)

Select SSH Username with Private Key

![image](https://github.com/devops-pritam/jenkins/assets/132892500/b259190c-f12d-49e1-aa9d-d0e8f431cafc)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/afe4c1f3-d30c-4b43-92c1-0c18c96bf640)


Click on Enter Directly and the ADD

![image](https://github.com/devops-pritam/jenkins/assets/132892500/40c23910-fc56-4699-b678-f8d456dd6f97)


Add the .pem file here

![image](https://github.com/devops-pritam/jenkins/assets/132892500/4c5d0420-6f2a-4081-90ab-f931e7d31852)


Click on ADD

![image](https://github.com/devops-pritam/jenkins/assets/132892500/2057aefe-289d-4119-9283-8b3ed8e61361)

Now, select the Credentials

![image](https://github.com/devops-pritam/jenkins/assets/132892500/d579073a-28fc-438e-8627-ac555eb87b92)

Select Non Verifying strategy

![image](https://github.com/devops-pritam/jenkins/assets/132892500/bb910cf0-d620-48b8-a18f-6df86e2764d2)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/3e31f2b6-f5b7-4ea9-bd11-db6b215f3acb)


clock on save

![image](https://github.com/devops-pritam/jenkins/assets/132892500/2958b091-3a6f-43db-a6c7-c1e7c8665dfb)

Jenkins slave is added

![image](https://github.com/devops-pritam/jenkins/assets/132892500/cf345caf-1d49-4e09-aa45-aca3eb432929)

Agent connected successfully

![image](https://github.com/devops-pritam/jenkins/assets/132892500/b0644185-c207-4fd9-8784-a33e34181406)

Slave in sync

![image](https://github.com/devops-pritam/jenkins/assets/132892500/7fa27449-ecc7-46d2-bfa3-bdb2d1ab9b22)

Create a pipeline job

![image](https://github.com/devops-pritam/jenkins/assets/132892500/17fb6f20-d817-45d6-a895-85f48a8c6ce3)

Write the script like this

![image](https://github.com/devops-pritam/jenkins/assets/132892500/d96011a2-2feb-49a3-845f-9e232b2e1c8a)

Apply Save 

Build now

Running this job in the slave 
![image](https://github.com/devops-pritam/jenkins/assets/132892500/5ee6abdd-bebd-4a75-b8a2-ff2e180cc500)


















































