
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
             
              aws deploy create-deployment --application-name chatappcodedeploy --deployment-group-name chatAppCodeDeployGP --deployment-config-name CodeDeployDefault.AllAtOnce --region-name us-east-2 --github-location repository=Bhushan1402/newChatapp,commitId=${GIT_COMMIT} 
             '''
            }
        }
    }
}
