Setup Jenkins

sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo
  sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key

These 2 commands can change time to time, So we need to visit the jenkins download page and run these 2 commands 

1) download java in amazon linux OS : sudo amazon-linux-extras install java-openjdk11 -y

2) Check the java version java --version

3) Java installation location :cd  /usr/lib/jvm
4) name of the java version : ls

sample : java-11-openjdk-11.0.18.0.10-1.amzn2.0.1.x86_64

5) cd ~

add your java version here and run the Echo command
--------------------------------------------------
6) echo "JAVA_HOME=/usr/lib/jvm/java-11-openjdk-11.0.18.0.10-1.amzn2.0.1.x86_64/" >> .bash_profile
7) cat .bash_profile
8) exit
9) sudo su -
10) echo $JAVA_HOME
11) Install jenkins : yum install jenkins -y

12) Check the status of Jenkins : sudo service jenkins status
13) Start the Jenkins : sudo service jenkins start
14) Get the Public IP : curl ifconfig.me.

Copy the public ip of our EC2 system , Go to the browser and paste the IP:8080



![image](https://github.com/devops-pritam/jenkins/assets/132892500/93d0d104-9101-490d-9e2d-61424eb69f12)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/f66db71c-b5f6-4a09-9173-e88cd2f68b83)


![image](https://github.com/devops-pritam/jenkins/assets/132892500/833e7bf0-3a54-4cd5-8355-0640eb1ddc4a)

Create a New Jenkins Job

Click on New Item
![image](https://github.com/devops-pritam/jenkins/assets/132892500/7abf71e1-56d9-4878-8122-48cfe49ec21f)

Select the Freestyle Project

![image](https://github.com/devops-pritam/jenkins/assets/132892500/05c5e792-807b-4d6f-ab47-73b9cc36ed38)

Lets run this job in every 2 mins (*/2 * * * *)
![image](https://github.com/devops-pritam/jenkins/assets/132892500/0431c729-cefe-4aad-9352-fc6fae56a4b2)

Now, in the build step Execute Shell
![image](https://github.com/devops-pritam/jenkins/assets/132892500/d7becffc-5cb4-4572-aec3-83578adedbfe)

echo "today's date and time is : $(date +%Y%m%d %H:%M:%S)"

![image](https://github.com/devops-pritam/jenkins/assets/132892500/8dc8de13-7584-4cf3-bf68-90bf89cf610c)

dt=$(date '+%d/%m/%Y %H:%M:%S')
echo "Todays Date and Time : $dt"

Now Build this JOB

![image](https://github.com/devops-pritam/jenkins/assets/132892500/77a22997-c5a4-4603-88ab-e59aea0cb871)

We will see the Build is Successful 
![image](https://github.com/devops-pritam/jenkins/assets/132892500/17f1678e-727f-498a-b6ea-7b9dda2884b7)

If we see console Output then

We can see the output
![image](https://github.com/devops-pritam/jenkins/assets/132892500/f89c28a9-8fb4-4111-986a-455a1367f44c)

Also we can see in every 2 mins the JOB is running as cron pattern we schedule the job like this

![image](https://github.com/devops-pritam/jenkins/assets/132892500/ffa44a9a-bf7a-4ffa-ac19-9303f1cb91c6)
















