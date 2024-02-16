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

Setup Tomcat Server in Amazon Linux 2

Launch Instance

![image](https://github.com/devops-pritam/jenkins/assets/132892500/964c965f-2f3b-4f97-a164-c7c62920902f)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/8dd413c3-35fa-4b33-92c9-185cda051438)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/30483c65-e826-454b-938e-1d69e244a385)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/8130e9f0-d534-4c92-bc22-c1e0f432813a)

Launch the Instance

![image](https://github.com/devops-pritam/jenkins/assets/132892500/2d902a21-a84b-487b-b8b9-221e9ea9e25e)

Instance is Running

![image](https://github.com/devops-pritam/jenkins/assets/132892500/249eac70-c8df-4bbd-9c88-b11b40a54b0d)

Logged in Via MobaXterm

![image](https://github.com/devops-pritam/jenkins/assets/132892500/bf2223d7-12e0-45ca-97a5-9b5af2fa3b77)

Search with Tomcat Download

![image](https://github.com/devops-pritam/jenkins/assets/132892500/8d03798c-22e6-46ce-b445-2678917eec58)

Download Tomact 10

![image](https://github.com/devops-pritam/jenkins/assets/132892500/623e6dd3-a17f-4ffa-b190-e2b0cffce39c)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/a1bb90e5-ff42-4963-915b-9992bb435411)

Lets navigate to ec2-user directory and download the tomcat

![image](https://github.com/devops-pritam/jenkins/assets/132892500/7c427399-c48c-499e-83c5-dbeb26f4d9c7)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/b1c76e58-656b-4422-9fca-0dea91d1f01b)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/9113e326-9e43-4572-9835-5208d4be9a51)

Unzip it

![image](https://github.com/devops-pritam/jenkins/assets/132892500/540e324b-40a9-40fa-842a-2a1787f70afa)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/a3bd4255-90c2-48e7-9982-62252353a002)

Lets change the Name of the Directory for simplicity

![image](https://github.com/devops-pritam/jenkins/assets/132892500/b4889eb9-16b4-4e2a-935f-1d6e5375cde7)

AS tomcat is an Application server , without installing java we cannot access Tomcat

![image](https://github.com/devops-pritam/jenkins/assets/132892500/7efdb2a8-711d-4683-919d-8b4333c535da)

Check the Java Version

![image](https://github.com/devops-pritam/jenkins/assets/132892500/ac45ac26-cb13-4c9f-9d7c-7e387fc2d0c8)

Lets see which ports are listning from our system

As of now, these posrts are listning from our system

![image](https://github.com/devops-pritam/jenkins/assets/132892500/c666ff41-83af-4ca0-a7a6-d4dff76e0304)

Lets go to bin directory of tomcat and start the server 

![image](https://github.com/devops-pritam/jenkins/assets/132892500/eb6b29c7-3cc5-4526-80d0-b07d23fa6961)

Now check the LISTNING ports

Now, we can see java is listning in port 8080

![image](https://github.com/devops-pritam/jenkins/assets/132892500/f1e976cb-03e9-452b-aa64-497c5ed2adf5)

Now, use the public IP:8080

We can see tomcat server is up and running

![image](https://github.com/devops-pritam/jenkins/assets/132892500/4380c2e3-c217-4fc9-82b5-4005922f1a1f)

Now, if we need to start the Tomcat is other ports than 8080 then we need to go inside conf directory

![image](https://github.com/devops-pritam/jenkins/assets/132892500/7e6b8469-911d-4298-97f3-426b029eb7fe)

Now open the file server.xml

![image](https://github.com/devops-pritam/jenkins/assets/132892500/c9c1e349-a346-491c-84b9-80def7966832)

Here we can see the connector port is 8080

![image](https://github.com/devops-pritam/jenkins/assets/132892500/b04033ae-af35-49d9-a980-3777ebdeff92)

Lets use the PORT 8090

![image](https://github.com/devops-pritam/jenkins/assets/132892500/15bdb23d-782d-4426-ac64-2fc8b6e4904f)

Save the file and restart tomcat server

![image](https://github.com/devops-pritam/jenkins/assets/132892500/9517c950-133d-45ff-85c1-b76819111fa6)

Now, we cannot see the tomcat is running 8080

![image](https://github.com/devops-pritam/jenkins/assets/132892500/23739a24-ad3c-4d17-b061-981ed24d0e2a)

Instead it is running in port number 8090

![image](https://github.com/devops-pritam/jenkins/assets/132892500/daa5ec72-025b-426e-aeba-b05367d72dce)

We can also see the port is listing on 8090

![image](https://github.com/devops-pritam/jenkins/assets/132892500/b5f60c55-1538-44ee-adc6-26f2fcbc80ca)

Now, click on the Manage App

![image](https://github.com/devops-pritam/jenkins/assets/132892500/8bba571e-2944-4133-9b73-848ab33aa431)

And there is an ERROR (403 Access Error)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/546cd757-f048-46bc-a0b1-18ee119ce15e)

In order to access by USER we need to configure this File

![image](https://github.com/devops-pritam/jenkins/assets/132892500/9f20910a-f882-49b5-9844-ee45c38ed5f5)

Lets Find this file

![image](https://github.com/devops-pritam/jenkins/assets/132892500/7e6fb8f9-652f-4d2b-b129-e31f61429651)

We need to consider only those files, which is under webapps directory

First edit this file

![image](https://github.com/devops-pritam/jenkins/assets/132892500/177ea2eb-b933-43fc-8ba6-a7938e87a757)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/9c42e21d-0a66-4d3b-a47b-3cb414e8d6d1)

Now Comment these 2 lines 

To comment <!--  -->

![image](https://github.com/devops-pritam/jenkins/assets/132892500/d684fb0a-4615-473e-b429-5cf497e359a1)
Save this file

Do it for all the Files 

Then restart the Tomcat 

![image](https://github.com/devops-pritam/jenkins/assets/132892500/2c7baf5d-1e6f-4cc1-9799-abff3ee9236a)

Now, if we click on Manage APP, Then we cannot see the Error, Instead it is asking for Username and Password

![image](https://github.com/devops-pritam/jenkins/assets/132892500/a6c24197-84dd-4b6d-92c8-2222e1456783)

Here we need to add some Roles for accessing the Tomcat Server 

Add these roles

 <role rolename="manager-gui"/>
 <role rolename="manager-script"/>
 <role rolename="manager-jmx"/>
 <role rolename="manager-status"/>
 <user username="admin" password="admin" roles="manager-gui, manager-script, manager-jmx, manager-status"/>
 <user username="deployer" password="deployer" roles="manager-script"/>
 <user username="tomcat" password="s3cret" roles="manager-gui"/>

Lets Navigate to the conf directory
 ![image](https://github.com/devops-pritam/jenkins/assets/132892500/7967bfc3-9f13-4950-bee8-8963afe96f2c)

 Here, edit this file : tomcat-users.xml

 Now, This is the users block and below this we need to add the roles of the users

 ![image](https://github.com/devops-pritam/jenkins/assets/132892500/02aa33b1-00b2-40d1-a1b2-225a16b84e01)

 Save this file

 Lets restart the Tomcat Server

 ![image](https://github.com/devops-pritam/jenkins/assets/132892500/b2eb37aa-1482-436a-b63a-86c3571a25e0)

 Click on manage app

 ![image](https://github.com/devops-pritam/jenkins/assets/132892500/9b8d1e6a-8a7f-431a-b975-ad016a0ea878)

 Now, lets login with admin ID and Password

 ![image](https://github.com/devops-pritam/jenkins/assets/132892500/8381630e-2d1c-462e-81a9-982790f263c9)

 Here we can see the Application Page,
![image](https://github.com/devops-pritam/jenkins/assets/132892500/70a25efa-29cf-4f0e-84a1-d23447974e9b)

 So this TOMCAT setup is DONE





 

























































































