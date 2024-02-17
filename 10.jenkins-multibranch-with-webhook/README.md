Here we are going to understand how can we enable AUtomated build when there is a change in the REPO

For that we need to enable Multibranch Scan Webhook

For that we need one Plugin Multi Branch Scan Webhook Trigger

Manage Jenkins

![image](https://github.com/devops-pritam/jenkins/assets/132892500/76d30fc1-a3b0-4a79-95bd-274e9b50d222)

Plugins

![image](https://github.com/devops-pritam/jenkins/assets/132892500/8aaf0a72-8ee7-496d-b2ca-40431c952b1f)

Lets Install this Plugin

![image](https://github.com/devops-pritam/jenkins/assets/132892500/fe6c1d80-e401-401a-89a2-c797ed0d4152)

Now, lets Enable the Webhook for our Job

Lets Open our Job

![image](https://github.com/devops-pritam/jenkins/assets/132892500/b02532e9-e647-40de-8fe1-659d0f555851)

Click on COnfigure

![image](https://github.com/devops-pritam/jenkins/assets/132892500/42d01c02-11f7-4b68-8ab9-d44b062c0f67)

Check the Checkbox Scan By Webhook and give the Token

![image](https://github.com/devops-pritam/jenkins/assets/132892500/2b563c03-392d-4f8c-bc5a-458ba58d9f77)

This is the help given by Jenkins



![image](https://github.com/devops-pritam/jenkins/assets/132892500/1cf41812-4d47-4ced-b633-3691c2771da9)

Open the Github Project and click on Settings

![image](https://github.com/devops-pritam/jenkins/assets/132892500/e2c6b26a-5fbd-4ded-a8c6-b3d9d5f51f4c)

Then Select Webhooks
![image](https://github.com/devops-pritam/jenkins/assets/132892500/9ab270b4-b0da-4cb6-8fc8-13b13592013d)

Here we need to Add our Webhook

![image](https://github.com/devops-pritam/jenkins/assets/132892500/c5844994-87c9-4bf5-8abf-bc73c352bac8)

JENKINS_URL/multibranch-webhook-trigger/invoke?token=[Trigger token]

lets modify the url as per our data

http://3.111.53.182:8080/multibranch-webhook-trigger/invoke?token=webhook-token

copy this and use it in Github

And make the content type as application/json

![image](https://github.com/devops-pritam/jenkins/assets/132892500/28a867e2-f3c9-4c8e-b04c-d3af07a7c67d)

Click on Add Webhook

![image](https://github.com/devops-pritam/jenkins/assets/132892500/c8b736a0-b0db-40e0-a81d-4bcb8f0a3fe3)

Here we can see as a Tick mark, that means it is connected successfully

![image](https://github.com/devops-pritam/jenkins/assets/132892500/8f045f48-6a92-4a3d-af41-ec37d0471080)

Now make a Change in any 1 Branch,

Lets make change in the PROD Branch

![image](https://github.com/devops-pritam/jenkins/assets/132892500/512a11d7-b5b0-4031-8005-a41144f62ccf)

Commit the changes

![image](https://github.com/devops-pritam/jenkins/assets/132892500/89a649d2-2e5d-4309-bc1a-b3303b1ce0d8)

Here we can see the PROD branch executed few seconds Ago

![image](https://github.com/devops-pritam/jenkins/assets/132892500/9c8bf129-5c61-4b32-bb64-8fe31d71a481)


















