pipeline {
  agent any
    stages {
        stage('Pull') {
             steps{
                script{
                    checkout([$class: 'GitSCM', branches: [[name: '*/master']],
                        userRemoteConfigs: [[
                            credentialsId: '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',
                                url: 'https://github.com/326-163/CDApp.git']]])
      		          }
     		       }
        		}
           }
      }
