
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
            
              aws deploy create-deployment --application-name ChatApp --deployment-group-name CFChatApp --deployment-config-name CodeDeployDefault.AllAtOnce --github-location repository=Bhushan1402/newChatapp,commitId=${GIT_COMMIT} 
             '''
            }
        }
    }
}
