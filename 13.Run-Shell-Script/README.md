Pre-requisite

Should AWS CLI Installed

![image](https://github.com/devops-pritam/jenkins/assets/132892500/ba06fe47-69aa-4628-ad06-e4d8c48a1c9b)

To install AWS CLI in server, the link

https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html

Select the Operating System , Here we are choosing Linux

![image](https://github.com/devops-pritam/jenkins/assets/132892500/27e6c390-f32b-4e69-8174-b410c6cacec9)

Then Run These commands :
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install

Then we can verify the installation by 

which aws

or

aws --version

![image](https://github.com/devops-pritam/jenkins/assets/132892500/3e424450-7162-44fe-9d72-d93b9d92a321)

Then configure AWS from this server

We need to have user in the AWS and from that user we need to get the Access Tokens.

After that 

Configure AWS from the Linux server with aws configure command

![image](https://github.com/devops-pritam/jenkins/assets/132892500/e9884ed9-87e8-4307-84c9-1e7aed46be9b)

Once thi is Done, we can see .aws directory and under that we can have 2 files , 
one) vonfig
two) credentials

![image](https://github.com/devops-pritam/jenkins/assets/132892500/96541053-7b64-47f8-9047-b7f6af4f0ccb)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/fbcc5065-cd80-4b00-a0a6-eb1762f0f223)

Now we can run the aws cli commands to get the AWS Informations.

For example, if we need to see all the AWS CLI commands related to IAM service, We can search with 

![image](https://github.com/devops-pritam/jenkins/assets/132892500/960bb43a-752a-4121-a8b3-1ca3cc56fc25)

Now, we can see all the AWS IAM service commands 

![image](https://github.com/devops-pritam/jenkins/assets/132892500/c7fe0b5b-932c-4f35-9256-640fbd8e39c1)

now, if we want to see which is the current user, we have to run this command

aws iam get-user

This is the current user

![image](https://github.com/devops-pritam/jenkins/assets/132892500/302ce67f-12b7-45eb-babe-0bc0e24d4a32)

If we want to see all the users present in IAM then,

![image](https://github.com/devops-pritam/jenkins/assets/132892500/61aaad85-b5a2-4f74-9d55-2ad3c1d9f42a)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/7a158374-46b8-4e57-9f6b-f50ca44866ac)

Similarly , if we need to see EC2 Service related commands

![image](https://github.com/devops-pritam/jenkins/assets/132892500/67cf2a8c-77f9-43b3-af84-d73557c8c66d)

Here we can see all the EC2 related Available commands

![image](https://github.com/devops-pritam/jenkins/assets/132892500/7831d6d6-9edd-41cc-8f5d-40cf8412c1be)


Now, if we need to see the details of the EC2 servers, then we can use this command

aws ec2 describe-instances

Here, we can see all the details

![image](https://github.com/devops-pritam/jenkins/assets/132892500/f5d7ff42-597b-4ebe-b5a5-47705de96699)

If we want to see all the cloudwatch related commands, 
![image](https://github.com/devops-pritam/jenkins/assets/132892500/409ab75c-779f-40ce-ad55-b9d6255d33e2)

Here we can see all the related commands

![image](https://github.com/devops-pritam/jenkins/assets/132892500/fc90c1f2-b207-4b69-a2d5-b0db53aa273a)

If we want to see the List of Dashboards, we can use 

aws cloudwatch list-dashboards

![image](https://github.com/devops-pritam/jenkins/assets/132892500/08a534fa-8cc2-40bc-93c1-c058ab2a966b)

If we want to see all the s3 Related commands ,

![image](https://github.com/devops-pritam/jenkins/assets/132892500/538b921e-0417-41b6-b9d1-079089dff16f)

We can see all the topic wise commands

![image](https://github.com/devops-pritam/jenkins/assets/132892500/35bddc00-2cce-413d-990d-17c5677ec939)

For Example we need to check the list of s3 buckets

aws s3 ls

![image](https://github.com/devops-pritam/jenkins/assets/132892500/f6d8139b-d6d3-420f-9637-817a55173786)

Now, everything we are doing manually, same details we can fetch via script also 

For that,

Create a Shell SCript

![image](https://github.com/devops-pritam/jenkins/assets/132892500/44323968-7d05-4708-9962-c5c6f8f72c3a)


![image](https://github.com/devops-pritam/jenkins/assets/132892500/68732a9f-7ed7-49fa-a22b-5e0a76b52129)

Give the executeable permission

![image](https://github.com/devops-pritam/jenkins/assets/132892500/d214be23-23eb-4bc7-8d86-44658d0daa23)

Now, execute the script

![image](https://github.com/devops-pritam/jenkins/assets/132892500/8b35a203-7019-49bf-a6c4-33fc13bb0a9a)

Now, lets run the script from Jenkins Pipeline

Create a pipeline

![image](https://github.com/devops-pritam/jenkins/assets/132892500/0f0e454e-e283-4b18-871c-23aaafdb5c41)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/b502621b-397b-4157-b812-7611cfa29a6a)


Apply Save and Build Now

Job is running

![image](https://github.com/devops-pritam/jenkins/assets/132892500/0268be2d-7246-47a9-b180-144210740010)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/95cf6356-c849-4f37-9f43-a330107abe74)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/93f2791f-872d-4ab3-abdf-77d6fd0bdab1)



































