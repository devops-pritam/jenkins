Check the Status of Jenkins

![image](https://github.com/devops-pritam/jenkins/assets/132892500/6281782c-298f-4517-8170-681fedf245b6)

Start Jenkins Server if that is not running

![image](https://github.com/devops-pritam/jenkins/assets/132892500/179c8f2d-a5b7-4cf1-8d07-bc72f48b0f4e)

Now, access Jenkins from Console

![image](https://github.com/devops-pritam/jenkins/assets/132892500/9fe27452-7fcb-463e-bcf0-1019a0e8d8ec)

We are under the Root Directory

![image](https://github.com/devops-pritam/jenkins/assets/132892500/bb172bcd-37fe-4631-94f1-548a1f6bf43d)

Create a directory named scripts and navigate inside that

![image](https://github.com/devops-pritam/jenkins/assets/132892500/90797b68-190e-4697-9c6f-621af40e5bca)
Lets Create A Script

![image](https://github.com/devops-pritam/jenkins/assets/132892500/9e81023a-cd8e-4057-b683-12d8634ed8ed)

Lets Write a Very basic script

![image](https://github.com/devops-pritam/jenkins/assets/132892500/8b632bfb-04c7-45a9-a28d-aa85d5cf11c6)

The owner of this script is root user

Give the Executable Permission to the Script

![image](https://github.com/devops-pritam/jenkins/assets/132892500/4dec261a-5ff6-41fd-8f43-ef0068989f9d)


Lets run the script from Local first

![image](https://github.com/devops-pritam/jenkins/assets/132892500/f9f87369-161e-4f83-9ee2-bdf2638b5163)

And it executes successfully

Now, lets navigate to the Jenkins

Lets Create A JOB

![image](https://github.com/devops-pritam/jenkins/assets/132892500/c200d47a-36eb-48c5-b6c7-ee808545abc8)

Lets Create A Pipeline SCript

![image](https://github.com/devops-pritam/jenkins/assets/132892500/79056666-4fe3-40bc-b8e8-ae7bfed35399)

Take the Hellow World as A Example SCript

![image](https://github.com/devops-pritam/jenkins/assets/132892500/aea4b71b-6faa-4b14-a199-30731c67e050)

Lets ReWrite this Pipeline like this

![image](https://github.com/devops-pritam/jenkins/assets/132892500/90a1607e-516b-479c-aa5e-689f07d119f4)

Apply Save

![image](https://github.com/devops-pritam/jenkins/assets/132892500/c9af395d-3329-488f-8bf8-36a7f1f29d36)

Build Now

![image](https://github.com/devops-pritam/jenkins/assets/132892500/51611786-a6f7-44dc-b727-fd8219559f7e)

We can see The issue is Permission Denied

![image](https://github.com/devops-pritam/jenkins/assets/132892500/e7f35fe3-84db-458e-af96-67c948997121)

If we open the CLI, we will see 1 user is there called jenkins 
![image](https://github.com/devops-pritam/jenkins/assets/132892500/c24c1aaf-3194-4170-9d74-ae9171640d49)
![image](https://github.com/devops-pritam/jenkins/assets/132892500/312f7647-ff47-4097-b654-83a2c589aa5b)

And we need to give jenkins the root previlages

![image](https://github.com/devops-pritam/jenkins/assets/132892500/48f608f3-4caf-4996-9a45-5cfdee2bb5db)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/750a4330-5888-41ce-9b7a-78bee6da7831)


Now rewrite the Script like this

![image](https://github.com/devops-pritam/jenkins/assets/132892500/c2870ea2-9582-44d9-80ff-00d9e4831d21)

Build Now

![image](https://github.com/devops-pritam/jenkins/assets/132892500/3da6382a-8682-4f43-96cc-7a1057e322b7)

























