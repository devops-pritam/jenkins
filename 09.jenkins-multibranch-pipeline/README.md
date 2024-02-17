Jenkins Multi branch Pipeline

What is Multibranch Pipeline

The Multibranch Pipeline project type enables us to implement different Jenkinsfiles for different branches of the same project.
In a Multibranch Pipeline project, Jenkins automatically discovers, manages and executes Pipelines for branches which contain a Jenkinsfile in source control.

This is the repo where we have 2 Branchs as of now Main and dev
https://github.com/devops-pritam/jenkins-multibranch

![image](https://github.com/devops-pritam/jenkins/assets/132892500/7d505988-ccd6-416c-b312-ca66c7f0b946)

and 

![image](https://github.com/devops-pritam/jenkins/assets/132892500/411c65dc-60ba-4162-a1db-fc96cc8d69e8)

So whenever we create a multibranch Pipeline for this repo, it should create 2 Piplenines, for each branch.

Lets start the Jenkins

![image](https://github.com/devops-pritam/jenkins/assets/132892500/12e65343-ca1a-47c9-8ebd-090fcc09fa6d)

Create a Pipeline , with multibranch 

![image](https://github.com/devops-pritam/jenkins/assets/132892500/784b8613-fee3-4988-ba7d-bd550aa5f6e8)

Click on Add Source

![image](https://github.com/devops-pritam/jenkins/assets/132892500/23e5b017-8b8b-4688-a6b1-14485c7809bb)

Select GIT

![image](https://github.com/devops-pritam/jenkins/assets/132892500/a56a9ed5-63d7-4b7a-90cf-a6f475ca6743)

Provide the Git Repo URL

![image](https://github.com/devops-pritam/jenkins/assets/132892500/e7326194-568c-4764-adba-6df93842a956)

Build Configuration, By Jenkinsfile

Means whereever it will find this file Jenkins is going to create the Pipeline

![image](https://github.com/devops-pritam/jenkins/assets/132892500/9d5c74cd-f753-49d5-8e76-b4e749e101f2)

Lets Apply and Save
![image](https://github.com/devops-pritam/jenkins/assets/132892500/5d5c2927-db47-4109-9340-54a4430bcf5b)

So now, it should create 2 Pipelines for 2 Branches as we have Jenkinsfile for both of our branches

Now, when we refresh we can see 2 Pipelines

![image](https://github.com/devops-pritam/jenkins/assets/132892500/875ee0b4-51f4-4721-8b19-60ec3aef3f11)

So, these pipelines are created and executes successfully.
![image](https://github.com/devops-pritam/jenkins/assets/132892500/b8cc39fe-6fc1-40bc-aec0-1825869e53ae)


Now, we need to check if we create a new Branch weather a new Pipeline creats or not

Lets Click on New Branch

![image](https://github.com/devops-pritam/jenkins/assets/132892500/fd82b6cc-6a49-4645-8291-a682783c0107)

Lets Create a New Branch nammed PROD

![image](https://github.com/devops-pritam/jenkins/assets/132892500/a060a76a-cc43-43b8-9946-c691af0a7315)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/b480cf57-3181-4bb8-a6ac-528c3dcf7157)

Lets Go to jenkins and Scan Multibranch Pipeline Manually

![image](https://github.com/devops-pritam/jenkins/assets/132892500/f765b038-ef5f-4045-a7b8-99a171e930ac)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/5e66bbf7-e0e4-4860-b0b1-ec00d4fcb4dd)

Here we can see the Build is in Queue

![image](https://github.com/devops-pritam/jenkins/assets/132892500/ade0bfc2-1ffa-4200-852d-3df8425e598a)

Now we can see the pipeline is creating

![image](https://github.com/devops-pritam/jenkins/assets/132892500/e0cb4499-1e95-4041-b9e8-6feb47fb0a77)























