Setup git in the EC2 Server

![image](https://github.com/devops-pritam/jenkins/assets/132892500/5b4ec212-a7c3-454e-9437-5ae1989cd080)

Check the git version

![image](https://github.com/devops-pritam/jenkins/assets/132892500/37aaad07-a46e-4550-92b3-cc001689aa4a)

Create a Pipeline

![image](https://github.com/devops-pritam/jenkins/assets/132892500/d8440041-a978-41bd-93b2-8a7431601a59)

Script
![image](https://github.com/devops-pritam/jenkins/assets/132892500/9a203b9e-0a1b-4652-841e-20a26aa6a9bc)

pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        
        stage('Application Versions') {
            steps {
                sh """
                    java --version
                    git --version
                    """
            }
        }
    }
}

Apply SAVE

![image](https://github.com/devops-pritam/jenkins/assets/132892500/a6c1c635-0831-46db-a1f0-fa43f6223f83)

Build Now

![image](https://github.com/devops-pritam/jenkins/assets/132892500/7fe30293-6843-4db1-a68e-5f2fc0e84321)

Console Output

![image](https://github.com/devops-pritam/jenkins/assets/132892500/62220f12-3bfe-4735-b79d-2c9a5ea9b76a)

Now, modify this script 

![image](https://github.com/devops-pritam/jenkins/assets/132892500/da5371c5-758e-47c9-ae26-c73ccd5540e8)

pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        
        stage('Application Versions') {
            steps {
                script {
                    
                    def response = input messege: 'Should we print the Java Version ?',
                    parameters: [choice(choices: 'yes\nno',
                    description: 'Proceed or Abort?',
                    name: 'What to Do?')]
                    
                    if (response=='yes') { 
                        sh """
                            java --version
                            git --version
                            """
                    }
                }
            }
        }
    }
}

Apply + SAVE

![image](https://github.com/devops-pritam/jenkins/assets/132892500/4160ebe1-eb38-4670-a0df-1c1d966ec06a)

Build Now

![image](https://github.com/devops-pritam/jenkins/assets/132892500/a8eb7160-e561-4d2b-84a8-620968146ed8)

We can see the Application Stage is Paused

![image](https://github.com/devops-pritam/jenkins/assets/132892500/0222d97f-370a-4b73-97ef-c7872bab8fa6)

If we mention Yes then the Stage will execute

![image](https://github.com/devops-pritam/jenkins/assets/132892500/285b00f8-9739-4cbe-ba5a-1a3c32baecba)

Build Passed

![image](https://github.com/devops-pritam/jenkins/assets/132892500/768ce81d-5f57-4c13-a60f-7ef264815b46)

Console Output

![image](https://github.com/devops-pritam/jenkins/assets/132892500/6a22e960-052c-414c-82bd-cd4358523a3c)

Click on Build Now Again

![image](https://github.com/devops-pritam/jenkins/assets/132892500/97c36425-af66-46cc-9727-f6a8e8029086)

Now Select No, and Execute

![image](https://github.com/devops-pritam/jenkins/assets/132892500/8274d4d0-c022-41e2-91c1-79c7f0351cf8)

And there is no Output

![image](https://github.com/devops-pritam/jenkins/assets/132892500/e50e2661-c972-422e-9957-db9948a0b807)

Open the OLD Jenkins Project

![image](https://github.com/devops-pritam/jenkins/assets/132892500/1a8cd8d8-cdd5-478c-870f-b01f666deb62)


Click on Configure

Click on Post Build Option and Build Other Project

![image](https://github.com/devops-pritam/jenkins/assets/132892500/491d1194-17ac-4212-b683-441acb8b3459)

Now, Select the old Other Job Here

![image](https://github.com/devops-pritam/jenkins/assets/132892500/eb608fbf-af4f-4fe9-ae68-36cb41dcbf1f)

Apply + SAVE

![image](https://github.com/devops-pritam/jenkins/assets/132892500/463682bd-da30-4a66-851d-ce008ed5dee5)

Now, run this job with yes parameter

![image](https://github.com/devops-pritam/jenkins/assets/132892500/d4d091f4-f775-4400-8f6a-f9754da6dece)

Build Success

![image](https://github.com/devops-pritam/jenkins/assets/132892500/57291650-d6a8-448e-b586-c30be3d77a77)

And we can see the other Job is Running and waiting for the User Input

![image](https://github.com/devops-pritam/jenkins/assets/132892500/604615c9-7af7-4c04-964d-82657685695b)

Yes And Procced

![image](https://github.com/devops-pritam/jenkins/assets/132892500/66483ef0-6a06-4790-86e0-5ad2a8fa3532)

And it executed Successfully 



























