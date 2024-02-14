Setup Maven in Jenkins Server

![image](https://github.com/devops-pritam/jenkins/assets/132892500/fd0c728e-5a4b-4ef0-8497-fdc7a56eb2c1)

Download the .tar file for Maven

![image](https://github.com/devops-pritam/jenkins/assets/132892500/5384c1d7-8a50-42ba-b022-e201198bca28)

Copy Link Address

https://dlcdn.apache.org/maven/maven-3/3.9.6/binaries/apache-maven-3.9.6-bin.tar.gz

![image](https://github.com/devops-pritam/jenkins/assets/132892500/e3e0b6a5-3d18-46d1-8cb0-6f36979be735)

Now, untar the tar file

![image](https://github.com/devops-pritam/jenkins/assets/132892500/d70c66c2-631a-4d94-a2f3-64e3c9e2dac4)

rename the directory name as maven

![image](https://github.com/devops-pritam/jenkins/assets/132892500/b12c088b-363c-444d-b6d2-1d6290de3652)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/3fa71282-1882-4541-8840-c2828d2cbf93)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/0aa2dcbd-9286-4442-a472-fc10ff009d72)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/85d989d6-c1e9-44b9-ab51-b176cf5348c3)

First Install GIT Plugin

![image](https://github.com/devops-pritam/jenkins/assets/132892500/5f8a46d3-81be-45f3-9b25-f6634fa759bc)

Now, Install Maven Plugins


![image](https://github.com/devops-pritam/jenkins/assets/132892500/2988902b-3ccc-49cc-b21e-d0b293fb1af7)

and

![image](https://github.com/devops-pritam/jenkins/assets/132892500/381db271-52ee-4bdd-9756-f498faebf000)

Now, Go to Manage Jenkins and Tools

![image](https://github.com/devops-pritam/jenkins/assets/132892500/e4a15c81-9383-4c0e-a074-d2e0ec62e0ad)

Click on Add Maven

![image](https://github.com/devops-pritam/jenkins/assets/132892500/e1077915-ab82-4e6f-a71c-a805338f9177)

Apply + Save

![image](https://github.com/devops-pritam/jenkins/assets/132892500/4cc2ea14-fda5-42b8-854a-620b73f31f8f)

Now Go to this Github (https://github.com/cameronmcnz/spock-lizard-docker)

Copy the Repo Link

https://github.com/cameronmcnz/spock-lizard-docker.git

Lets Create the Freestyle Project

![image](https://github.com/devops-pritam/jenkins/assets/132892500/b3e90d7f-3920-4843-a617-af457edac705)

Setup the Repo in Jenkins
![image](https://github.com/devops-pritam/jenkins/assets/132892500/a1943964-ef27-4695-bcdc-1f083bd3e980)

Click on Build Step and Invoke Top Level Maven Project

![image](https://github.com/devops-pritam/jenkins/assets/132892500/54e42523-bdee-4c9c-a9fe-de3c1e0b315c)

Set The Maven Goals

![image](https://github.com/devops-pritam/jenkins/assets/132892500/55b26d61-c6e7-487e-9df4-e686b175b77b)
![image](https://github.com/devops-pritam/jenkins/assets/132892500/7676c30a-60ad-4fc0-b5c1-93242a43fb5f)


Apply + Save

![image](https://github.com/devops-pritam/jenkins/assets/132892500/fb296e90-32c3-420e-9e0a-1b8ec01d4584)

Click on Build Now

![image](https://github.com/devops-pritam/jenkins/assets/132892500/8b318e65-318b-4ca0-9edf-b9cd9ce6ecbd)

Build Success

![image](https://github.com/devops-pritam/jenkins/assets/132892500/c4d59492-c188-4d53-8cf0-269e9c386a4d)



























