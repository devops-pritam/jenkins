Download Nexus

![image](https://github.com/devops-pritam/jenkins/assets/132892500/e58e30b7-49c2-4d37-a78e-8dd2f215de0f)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/37ac122a-7cb4-45d1-976b-e48af3705403)

Go to Product Information and the Download Link

![image](https://github.com/devops-pritam/jenkins/assets/132892500/d50e81d9-5723-4f81-9986-4c6c51399118)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/70f87556-948d-47b9-a373-a8c9a06205d7)

Launch Instance

![image](https://github.com/devops-pritam/jenkins/assets/132892500/64c3d813-b378-48ff-b3b2-f419dc7f1879)

select t2.medium

![image](https://github.com/devops-pritam/jenkins/assets/132892500/32432141-a0a0-49cd-976e-e35009551a14)

Lets Launch the Instance

![image](https://github.com/devops-pritam/jenkins/assets/132892500/c28164b7-f052-42ac-986e-b593577217a7)

Connect with the Terminal

![image](https://github.com/devops-pritam/jenkins/assets/132892500/a788e246-9126-4d18-a491-6f08dd6f56c1)

Navigate to the opt directory and download Nexus related packages

![image](https://github.com/devops-pritam/jenkins/assets/132892500/6b3548d6-45f5-42ad-b24b-239ca013e3a7)

Unix Archive Copy Link Address

![image](https://github.com/devops-pritam/jenkins/assets/132892500/0eff016e-c99e-46f2-9761-5c0eded1f709)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/0d52fa68-14ba-43f0-8ea6-0b43e450c785)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/23541d08-bef2-4d9a-bcc2-2a2f669e7e38)

Untar this Package

![image](https://github.com/devops-pritam/jenkins/assets/132892500/a794b20f-de07-47c9-a411-086d15e55653)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/e7d9f48f-089c-4398-adf6-68c3d25036d0)

Lets Rename the Folder Name for Simplicity

![image](https://github.com/devops-pritam/jenkins/assets/132892500/5c9e145f-81e4-4979-9370-b5f41322cae2)

Under the Nexus Directory we have the Binary Files

![image](https://github.com/devops-pritam/jenkins/assets/132892500/578fdb18-9121-407a-a2e0-31f58c887c6f)

Under the Bin directory we are having the options to work with Nexus

![image](https://github.com/devops-pritam/jenkins/assets/132892500/b3af09d0-a89e-49c2-bf62-49d3c305fb15)

But here both the Directories are owned by root user

![image](https://github.com/devops-pritam/jenkins/assets/132892500/e809bf10-5ff6-4b6a-9adc-4abb71f8d939)

We need to change the Ownerships

Now, lets create an user for nexus work along with the Password

![image](https://github.com/devops-pritam/jenkins/assets/132892500/91f27841-6e7e-44d5-9392-5ce6238a0a46)

Now, I do not want the user to use password to invoke the sudo commands

for that add this user to the sudo list

![image](https://github.com/devops-pritam/jenkins/assets/132892500/41ec1eee-ec5a-4ca1-84e5-8687bb8d3d9b)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/0c1d92e9-9a4d-4950-8df1-4a81ae26a35b)

Now, change the ownerships of the nexus related directories

![image](https://github.com/devops-pritam/jenkins/assets/132892500/90359c9d-0024-4260-b9c2-df13e3ba93ef)

Here, lets open the file nammed nexus.rc

![image](https://github.com/devops-pritam/jenkins/assets/132892500/2c30ae88-6789-46e7-889e-a17c749373ec)

This is the content of the File,

![image](https://github.com/devops-pritam/jenkins/assets/132892500/f864b98d-2758-4411-b863-cfd6ea446dea)

Lets Change it to :

![image](https://github.com/devops-pritam/jenkins/assets/132892500/818c1e57-96d3-44ab-bb76-e0cd01310381)

Save this File

In order to change the Nexus work, we need to make change in our Nexus Data DIrectory which is nexus.vmoptions

Open this file

We can change this directories to take the backup of our Nexus Data

![image](https://github.com/devops-pritam/jenkins/assets/132892500/88d51238-a1c8-4dba-85f0-448b69329ba8)

Now , in ordder to check the PORT details we need to navigate to the etc directory

![image](https://github.com/devops-pritam/jenkins/assets/132892500/37369955-bb3f-4970-a66d-9a102a2cbd38)

Here we have one file named : nexus-default.properties

open this file

Here, we can see the port details

![image](https://github.com/devops-pritam/jenkins/assets/132892500/d50b10e1-87c4-432f-a84f-8b7484e05f2f)

From the Nexus URL go to Installation and upgrade

![image](https://github.com/devops-pritam/jenkins/assets/132892500/76a2b390-e221-4c11-a5bf-198fc8af9f00)

Click Run As A Service

![image](https://github.com/devops-pritam/jenkins/assets/132892500/887b2af7-59f5-4945-8b0f-4d292367b91b)

Copy this 

![image](https://github.com/devops-pritam/jenkins/assets/132892500/a910eecc-3a6a-4515-ac68-aa6c6c4bf714)

Make the Changes into the Service file like this way

![image](https://github.com/devops-pritam/jenkins/assets/132892500/0bd79d7a-950d-4beb-9ee9-dc72be0e5b55)

Create the File like this 


![image](https://github.com/devops-pritam/jenkins/assets/132892500/21662a36-2baf-4dd7-a6fc-ea97789c074c)

Copy the Service file and paste it here 

![image](https://github.com/devops-pritam/jenkins/assets/132892500/227516e1-afd6-434e-bba8-572ac5b09bb5)

Enable Nexus

![image](https://github.com/devops-pritam/jenkins/assets/132892500/e9031f25-fbfd-4abf-9854-9fd2691c9339)

Now, lets update the yum package

![image](https://github.com/devops-pritam/jenkins/assets/132892500/ee6f0677-a5d4-42e2-bd4a-b086c20b810b)
And install JAVA 8 

sudo yum install -y java-1.8.0-openjdk-devel.x86_64

Check the JAVA Version
![image](https://github.com/devops-pritam/jenkins/assets/132892500/475e0c56-aef6-44c5-a65c-24c9eaf5ab1d)


Now, restart the nexus and check the status

![image](https://github.com/devops-pritam/jenkins/assets/132892500/fe998d0d-3630-431a-8a0b-c4ef66afd33d)

Nexus is up and running 

Now, use the public IP:8081 

![image](https://github.com/devops-pritam/jenkins/assets/132892500/4930944c-4d0f-44a8-bab5-a74ed04b3480)

It will take 2 mins of time to load the page

Once it opens, click on signin

![image](https://github.com/devops-pritam/jenkins/assets/132892500/c4f19f95-7e0f-437c-b76c-c55c73928e34)

And get the Password from this location

![image](https://github.com/devops-pritam/jenkins/assets/132892500/b28ed896-1a4a-468b-b8d6-461851b3f722)

Got the password

![image](https://github.com/devops-pritam/jenkins/assets/132892500/854e7975-7f63-4ef6-8c95-c1c84e5a2362)

Lets Login

![image](https://github.com/devops-pritam/jenkins/assets/132892500/dbb2094d-5760-4d3f-9363-d1856cad27ce)

Now, change the password

![image](https://github.com/devops-pritam/jenkins/assets/132892500/3a55dfed-ba2a-4855-9214-80bc47eb0418)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/82efa5b0-0170-4f76-a7aa-e2f9f0c1a43b)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/de507e02-2835-4fd9-b235-9c4f98cf3206)

So the Setup is DONE
















































