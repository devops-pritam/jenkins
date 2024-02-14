Jenkins Parameterize build Job

![image](https://github.com/devops-pritam/jenkins/assets/132892500/4978bbf1-3db0-47d0-8c8f-6599fe6f996e)

Create Freestyle Project

![image](https://github.com/devops-pritam/jenkins/assets/132892500/263e5f15-64ad-41ca-a99f-a87e77377887)

Check the Checkbox
![image](https://github.com/devops-pritam/jenkins/assets/132892500/ca0c9ccd-d2a2-4cfc-b470-7b6f1ac98936)

Here, we can see different parameters supported by Jenkins

![image](https://github.com/devops-pritam/jenkins/assets/132892500/8679be81-59c2-4ad4-affe-8917dda7e473)

Lets choose the Choice Parameter

![image](https://github.com/devops-pritam/jenkins/assets/132892500/f3d1673d-6e21-44ff-9ab8-15729c1517b5)

Put the Parameter name with the desired choices
![image](https://github.com/devops-pritam/jenkins/assets/132892500/8101988b-7d17-4779-b397-be68b96425f1)

Add build Step 


if [ $shouldWePrint="yes" ]
then
  java --version
fi
if [ $shouldWePrint="no" ]
then
  echo "DO Not Print"
fi


![image](https://github.com/devops-pritam/jenkins/assets/132892500/42381d7e-8232-42bd-ab08-448be2ebb106)


Apply and Save

![image](https://github.com/devops-pritam/jenkins/assets/132892500/4733dc01-802f-4393-a56a-244769365187)

Now Click in Build with Parameter
![image](https://github.com/devops-pritam/jenkins/assets/132892500/b8764cf0-986c-46ba-8836-4cc3837b3e35)

First, Build with yes choice

![image](https://github.com/devops-pritam/jenkins/assets/132892500/129f4e10-d09b-49da-9466-d8c72468cf0a)

We can see the Java Version
![image](https://github.com/devops-pritam/jenkins/assets/132892500/f4086e71-95d5-4cca-8632-9dacf06032a1)

Now build with no choice

![image](https://github.com/devops-pritam/jenkins/assets/132892500/b5c62ccc-a90e-4877-88f0-745ae97f48ab)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/df6d8efc-f672-4ba2-8604-8f7ed3d10179)



NOW LETS DO THE SAME IN THE PIPELINE JOB

OPEN THE PIPELINE JOB

![image](https://github.com/devops-pritam/jenkins/assets/132892500/2982051b-3eb9-4380-bb7c-9a11cd6f3cac)

Click on Configure

![image](https://github.com/devops-pritam/jenkins/assets/132892500/42a8d567-a12c-45fc-abb2-fce746cd3bf3)

Click on Pipeline Syntax

![image](https://github.com/devops-pritam/jenkins/assets/132892500/a65707d0-9f25-40b9-8634-8ffd589bbfd9)

Select set job properties like this 

![image](https://github.com/devops-pritam/jenkins/assets/132892500/77b19b6a-a130-45c4-9619-4302828394a2)

Provide the Details

![image](https://github.com/devops-pritam/jenkins/assets/132892500/48487853-249a-41a1-b59f-bb636fb7d94f)

Click on generate the Script

![image](https://github.com/devops-pritam/jenkins/assets/132892500/bc71bf1a-b391-4b88-9160-dd4bc2f6ab7d)

Copy this

![image](https://github.com/devops-pritam/jenkins/assets/132892500/c9fb95c5-5168-4035-88d9-257e1cb82f4c)

Now in order to run the Parameter we need to use the script block like this 

Full Script

![image](https://github.com/devops-pritam/jenkins/assets/132892500/d8ad2686-a93c-490b-af68-9df02f53a137)

=================
pipeline {
    agent any

    stages {
        stage('parameter') {
            steps {
                script {
                
                properties([parameters([choice(choices: ['yes', 'no'], name: 'shouldWePrint')])])
                        }
                  }
            
        
        }
        stage('Print') {
            when {
                expression { 
                   return params.shouldWePrint == 'yes'
                }
            }
            steps {
                    sh """
                    java --version
                    """
                }
            }
        stage('No Print') {
            when {
                expression { 
                   return params.shouldWePrint == 'no'
                }
            }
            steps {
                    echo 'No Print Required'
                }
            }
   }
        
    
}
==================
Apply and Save

![image](https://github.com/devops-pritam/jenkins/assets/132892500/07697cd6-9d53-4229-8536-959e13144291)

Build with yes Choice

![image](https://github.com/devops-pritam/jenkins/assets/132892500/f2a58685-53c3-431b-9c75-97daaa92f13d)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/95a88a8a-07b1-41b7-9488-9fad5bd4da89)

Build with No choice

![image](https://github.com/devops-pritam/jenkins/assets/132892500/2d94ce6c-8983-440a-84cb-e6be14ca56e9)

![image](https://github.com/devops-pritam/jenkins/assets/132892500/b7924f29-6ddf-4d02-91bc-fe600071fead)




























