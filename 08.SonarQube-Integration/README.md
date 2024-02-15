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

Lets do it Manually

![image](https://github.com/devops-pritam/jenkins/assets/132892500/12965b2d-2595-492c-99ff-0bbe6a14f60a)

Give some project name with some project key

![image](https://github.com/devops-pritam/jenkins/assets/132892500/7cf24cd6-6d42-4f96-ad82-1aa5726ae61b)

Click on Set Up
![image](https://github.com/devops-pritam/jenkins/assets/132892500/8d0da58b-7c6c-4136-8fb9-cb1233c0dcba)

Click on Test 
![image](https://github.com/devops-pritam/jenkins/assets/132892500/cdb694c8-a124-40cc-b1b6-5bea6eae653a)

And generate the Token

![image](https://github.com/devops-pritam/jenkins/assets/132892500/8c84b667-a168-41f2-97d5-7dec4a0b21a4)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/df6172fa-9ee9-40eb-951d-359c13ff5e23)

Copy this token

We can give this token for authentication

sqp_79b9fcec92e28e796c08211f7f451ec53b8056eb

If we click in continue, it will give the options
![image](https://github.com/devops-pritam/jenkins/assets/132892500/e19f7ee5-d6e8-4897-a66a-2951b7c052af)

For example, If we need to work with maven then choose maven and it will show the way to authenticate

![image](https://github.com/devops-pritam/jenkins/assets/132892500/6b98ce3e-ab0d-41ba-abc5-68b9cf9a2d64)

here we can see the rules, as it support different languages, it has different rules

![image](https://github.com/devops-pritam/jenkins/assets/132892500/b04282b9-70f0-4a24-936f-72c0cd4b02bd)

These are the languages and these are the rules depending on the Languages
![image](https://github.com/devops-pritam/jenkins/assets/132892500/b852c394-b496-4ddc-baea-d41a83f6be55)

These rules are being used to Crete the Quality Profile, Quality profile is nothing but the collection of rules

![image](https://github.com/devops-pritam/jenkins/assets/132892500/2e6f8ece-dbcc-4453-a551-2cdc2013987a)

Lets create the profile

![image](https://github.com/devops-pritam/jenkins/assets/132892500/b0893427-0f1d-4496-bf0b-108fa325fb6d)

Lets add these details

![image](https://github.com/devops-pritam/jenkins/assets/132892500/ad48970d-f7f0-4520-86c3-863bc5ccb629)

Lets Create it

![image](https://github.com/devops-pritam/jenkins/assets/132892500/541547a7-9474-417b-b8a5-04ef57db4de7)

At this moment we have these rules, some of the are active and some are inactive
![image](https://github.com/devops-pritam/jenkins/assets/132892500/7cf0fae4-7aa7-48e9-bd8d-a67f39143e47)

If we need more Active Rule then

![image](https://github.com/devops-pritam/jenkins/assets/132892500/6f04996b-1161-4ede-b205-bff936929af2)

Clickon Activate more and then Bulk option
![image](https://github.com/devops-pritam/jenkins/assets/132892500/685dd023-099b-4491-bf33-99935f0d5792)

Clickon Activate in Maven Profile
![image](https://github.com/devops-pritam/jenkins/assets/132892500/b3eee8f9-9e79-4266-b299-0ed2461ac3e1)

Click oN Apply

![image](https://github.com/devops-pritam/jenkins/assets/132892500/369dfb4e-2bd3-46fc-a964-e23f8ceb92c7)

Some Rules are changed but most of them Activated

![image](https://github.com/devops-pritam/jenkins/assets/132892500/65fbfc46-7937-432a-9194-95805aea9ea5)

If we need to set this as the Default Profile for java then we can make it Default Profile

![image](https://github.com/devops-pritam/jenkins/assets/132892500/03117942-2012-4517-af13-e0b08d47b58a)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/faf425d1-1a8a-4f26-8e42-413e428192bd)

So next time onwards, if we are going to do analysis for any Java Project it will be our Default Profile

In The Quality Gate, we can see the Threshould Value, Or the checkpoint to pass or fail the Development Codes

![image](https://github.com/devops-pritam/jenkins/assets/132892500/d015148f-4b2c-4b50-9b17-2bdb16d7f2d7)

We can create our Own Quality Gateway
![image](https://github.com/devops-pritam/jenkins/assets/132892500/f692824f-6d47-4205-81e0-82adc9466543)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/9279aae7-6a84-43bc-81e6-ecd0463da7a7)

Here we can Edit the Conditions

![image](https://github.com/devops-pritam/jenkins/assets/132892500/a068be5e-2451-4838-9910-62b2daaaf21a)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/1d00645f-2de2-4758-8c20-24eb4627026b)

Code Coverage Means What % of code is covered by Test Cases 
We can Make it as Default

![image](https://github.com/devops-pritam/jenkins/assets/132892500/49db27a4-d93c-46e4-b566-bd5a95fe7f72)

Now, Create a New Server and setup Maven

![image](https://github.com/devops-pritam/jenkins/assets/132892500/9a0f28b3-70d9-42f3-b0db-ebc6a73ef491)

Lets Clone a Github Repo

![image](https://github.com/devops-pritam/jenkins/assets/132892500/09e91d94-560c-4dd0-b044-fd4f84e77de0)

Now we need to run this code
![image](https://github.com/devops-pritam/jenkins/assets/132892500/ec864d24-6446-4d83-9a31-55db27f6ede4)

Because , we need to setup sonarscanner where our development code is present

Lets go to the Project folder and execute this command
![image](https://github.com/devops-pritam/jenkins/assets/132892500/47f50838-0b76-4f48-8fef-e7496133d8c1)


![image](https://github.com/devops-pritam/jenkins/assets/132892500/010f7d4a-baa3-46f4-9d07-3aeea1f777e9)

This is a big project so use a small project 

![image](https://github.com/devops-pritam/jenkins/assets/132892500/646e1619-6930-4b8a-8fed-f8a16771e8c9)

Run the Maven commands
![image](https://github.com/devops-pritam/jenkins/assets/132892500/c712aeb7-7b93-49eb-989a-fb3492be1891)

Build Success
![image](https://github.com/devops-pritam/jenkins/assets/132892500/d2ddd873-0c08-4712-b6d9-f4134fb91de6)

Lets Check the report
![image](https://github.com/devops-pritam/jenkins/assets/132892500/cafcd356-6f69-4151-aec2-5ffd66a82c1a)

Detailed Report

![image](https://github.com/devops-pritam/jenkins/assets/132892500/90cff650-c33d-456a-b43e-61434c65e881)








































































