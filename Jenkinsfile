
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
             
              aws configure [
                                AWS Access Key ID [None]: AKIARXBF57RSDU6OGR7Z
                                AWS Secret Access Key [None]: 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
                                Default region name [None]: us-east-2
                                Default output format [None]: json] 
              aws deploy create-deployment --application-name chatappcodedeploy --deployment-group-name chatAppCodeDeployGP --deployment-config-name CodeDeployDefault.AllAtOnce --github-location repository=Bhushan1402/newChatapp,commitId=${GIT_COMMIT} 
             '''
            }
        }
    }
}
