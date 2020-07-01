
pipeline {
    agent any
     stages {
     stage('Build') { 
           steps {
             echo "Bhushan"
            }
        }
         stage('Deploy') { 
           steps {
             sh ''' #! /bin/bash 
             
              aws configure --region us-east-2
              aws deploy create-deployment --application-name chatappcodedeploy --deployment-group-name chatAppCodeDeployGP --deployment-config-name CodeDeployDefault.AllAtOnce --github-location repository=Bhushan1402/newChatapp,commitId=${GIT_COMMIT} 
             '''
            }
        }
    }
}
