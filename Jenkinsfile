pipeline {
  agent any
    stages {
        stage('Pull') {
             steps{
                script{
                    checkout([$class: 'GitSCM', branches: [[name: '*/master']],
                        userRemoteConfigs: [[
                            url: 'https://github.com/326-163/CDApp.git']]])
                }
             }
         }

        stage('install') {
             steps{
                script{
                    sh " npm install --save-dev @angular-devkit/build-angular"
                }
            }
        }

        stage ('Build') {
   		steps {
			script {
			sh "ansible-playbook ansible/build.yml -i ansible/inventory/host.yml "
	        }
            }
         }


       }
      }
