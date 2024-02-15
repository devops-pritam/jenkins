SonarQube

In The Development phase developer write the code and we need to validate Developer has written the Quality Code or Not.

Quality Code is nothing but We need to check 

1) Is it Bug Free ?
2) Is it Secure or not ?
3) Are there any Duplication in the code or not ?
4) Is the code is tested properly or not ?
5) Have they written any Complex code or not ? If the code is complex then other people cannot read the code if they need to debug some issues .
6) Is it easy to integrate with other codes or not ? One developer code might be integrated with other developer's code

All these come under the Code Quality check, But all these checks who will do ? 

We can do it by Peer Review . But if the project is very big , in that case manual review is a very tedious task. We need some Kind of Automation which can help us to achieve these.

In this case we need to Use Static Code Analysis . 

Using this SCA we can reduce the manual effort as well as we can improve the code quality

SonarQube is one of the SCA tool available in the Market.

Why SonarQube ?

It is a Quality Management tool .

Apart from Code Analysis it can 
- Gather Test Reports
- Code Coverage Reports
It collects all the data and display in the GUI in a Good Understandable Manner

Components Of SonarQube
A) SonarQube Server (Where we are installing SonarQube)

1) Rules : Instractions we need to follow while writting our code (There are many default rules comes with the SonarQube installation)
2) Database : By using the rules we run our source code and with that we will get the Analysis Report, and the report should be kept under the Database.
3) Web Interface : Once the Analysis report is stored into the Database, Through the Web we can see and analysis the report very easily

B) SonarScanner 

SonarScanner should be present in that server where we have the development code. For Example, We have a Java Code, And we need the report, SO we need to install the SonarScanner in that server and run the Scan

This is the official SonarQube page : https://www.sonarsource.com/products/sonarqube/?gads_campaign=SQ-Hroi-PMax&gads_ad_group=Global&gads_keyword=&gad_source=1&gclid=CjwKCAiAibeuBhAAEiwAiXBoJCIlkD3FJt7bKbOxQppksi8pADe4vNrVsthvbdwdLRVFKlk7Kyz3JBoCuQsQAvD_BwE

Here we can see it supports these many Programming Languages

![image](https://github.com/devops-pritam/jenkins/assets/132892500/1faa2265-3df5-40c1-8fcc-7a3d7d9e0217)

Installation oF SonarQube

An EC2 instance with a minimum of 2 GB RAM (t2.small)
Launch EC2 

![image](https://github.com/devops-pritam/jenkins/assets/132892500/526f63fd-93f2-4697-8794-a238b13fc596)

Select Instance type as t2.small

![image](https://github.com/devops-pritam/jenkins/assets/132892500/efddd08a-a35c-4614-b764-4269f5dc45f6)

In My case I have opened all the Ports but, we need to make sure we need to open port number 9000 to access SOnarQube from the Browser

![image](https://github.com/devops-pritam/jenkins/assets/132892500/ffd0aa9e-aa4b-482c-a5b7-8cdae2977f93)

Server is Up And Running

![image](https://github.com/devops-pritam/jenkins/assets/132892500/b24717be-a834-4e80-81a9-d33a11431593)

Lets Cnnect,

Now, we need to Install Java

Java 11 installation:

amazon-linux-extras list
amazon-linux-extras install java-openjdk11 -y


![image](https://github.com/devops-pritam/jenkins/assets/132892500/f3312dcb-35fe-4228-bece-4a0b1004dbef)

Java install is successfull 

Check the Java Version

![image](https://github.com/devops-pritam/jenkins/assets/132892500/2897cec3-9481-405c-825f-679bb90d20fd)

SonarQube cannot be run as root on Unix-based systems, so create a dedicated user account for SonarQube if necessary.

cd /opt  
wget https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-x.x.zip 

![image](https://github.com/devops-pritam/jenkins/assets/132892500/30337d01-c836-4304-a8a2-04e151f225fc)

Search with Download SonarQube

![image](https://github.com/devops-pritam/jenkins/assets/132892500/35d7aa1c-e094-481e-a1da-6292d015713f)

This is the Latest Version
![image](https://github.com/devops-pritam/jenkins/assets/132892500/94e3a06e-117f-4072-b111-832ae2e93d4f)

Copy Link Address 

![image](https://github.com/devops-pritam/jenkins/assets/132892500/ef59f30f-2f39-4403-a8d7-498803fc79f0)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/3306203c-2aa0-4078-ac45-97e1662ff377)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/f75d8dfa-81eb-48c6-a346-42fa73faedc4)

Unzip the .zip file

![image](https://github.com/devops-pritam/jenkins/assets/132892500/12cd87cb-aad8-4092-a6c4-67bbe70970fb)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/bf73efe3-1692-404b-8cef-6cfab344b3c7)

Now, lets go inside of the conf directory 
![image](https://github.com/devops-pritam/jenkins/assets/132892500/d4cd434a-1e80-46a4-89fd-32b3df10b85b)

There are some pre defined Properties of the SOnarQube

![image](https://github.com/devops-pritam/jenkins/assets/132892500/f05c92ca-32ca-49e0-8e6f-9a065c392dd2)

If we are running the SOnar Database in some different server then we need to give the Id password details

![image](https://github.com/devops-pritam/jenkins/assets/132892500/a4b4fe73-8007-4919-8e9b-d2482eaaec18)

Here, we can see the sonar web is running in port 9000

![image](https://github.com/devops-pritam/jenkins/assets/132892500/b9b630d1-986d-4d08-b228-ec2ba2cf914c)

In the bin directory we can see SOnarQube can support different OS 
![image](https://github.com/devops-pritam/jenkins/assets/132892500/9ba8ca4a-f580-45a5-97fc-ffcf54dfd598)

In our case we are working with the Linux OS

Lets go inside the Linux Directory and inside that we have one .sh file which we need to start

![image](https://github.com/devops-pritam/jenkins/assets/132892500/df7027ed-da31-43f0-b975-d16f9c383d60)

Now, SonarQube doesnot run with the root user , We need to Create A New User for this

![image](https://github.com/devops-pritam/jenkins/assets/132892500/f78217fe-1fd8-45e0-81db-4c3632a20ab7)

Here, we can see the ownership of the file belogs to new user

Now, lets login with the sonaradmin user and start the .sh file

![image](https://github.com/devops-pritam/jenkins/assets/132892500/ce69e968-4dcb-4e78-be4c-64215ac0bfc5)

Check the Status

Now, if we need to check the log if there is any error then 
![image](https://github.com/devops-pritam/jenkins/assets/132892500/96434c47-aae1-4ea1-a4bc-200abcb39714)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/dad87828-b591-46fa-b5f2-dc2453aea943)


And if we need to uninstall java (any specific version)
![image](https://github.com/devops-pritam/jenkins/assets/132892500/5bc35eb7-d6d6-4878-98b9-1a201a107b46)

yum list java*

![image](https://github.com/devops-pritam/jenkins/assets/132892500/3e5000ab-4c3a-4353-af36-d97c8cb66616)

yum install java-17-amazon-corretto.x86_64 -y

![image](https://github.com/devops-pritam/jenkins/assets/132892500/df28a761-f625-448f-925b-79f7a0f93e43)
![image](https://github.com/devops-pritam/jenkins/assets/132892500/b90249a5-22c2-412f-9f3b-a39b18f27f49)

Now the sonarserver is running

Now Copy the Public IP of the CE2 with :9000 Port Number

![image](https://github.com/devops-pritam/jenkins/assets/132892500/1c15ac31-f5a5-4591-b26d-aec653716dd4)

netstat -tulpn | Using this Command we can see which port is opened

![image](https://github.com/devops-pritam/jenkins/assets/132892500/162428ed-ae7a-4929-a724-12c310affe9b)


By Default the userid and password is admin and admin
![image](https://github.com/devops-pritam/jenkins/assets/132892500/67a41cc4-7ab8-44c7-bb8a-e286a6963046)

in the 1st Login we changed the password 

![image](https://github.com/devops-pritam/jenkins/assets/132892500/54a6bb64-e25c-4846-ac2b-08456a0cbc79)

And this is the SonarQube Dashboard

![image](https://github.com/devops-pritam/jenkins/assets/132892500/3dcf8aab-56f7-4ee3-adb4-7ae2d5ad8be2)

Here, under this Projects we can mention which Project we need to Scan via SonarQube

![image](https://github.com/devops-pritam/jenkins/assets/132892500/d3e6df7e-2318-43ca-92b2-4a08056a9516)

We can also Connect out SCM here (From Github, Gitlab or BitBucket)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/52c0e8cf-5847-462a-bf13-6855dd423369)






























