pipeline {
    agent any

    stages {
        stage('clone repo') {
            steps {
                echo 'clone repo'
                sh 'rm -fr test_web'
                sh 'git clone https://github.com/renatasilva11/test_web.git'
            }
        }
    
   
        stage('push repo to remote host') {
            steps {
               echo 'push repor to remote host'
            }
        }
       
        stage('connect') {
        steps {
          sshagent(credentials: ['webfiles']) {
            sh 'ping ec2-34-245-42-100'
            
          }
      }
    }
  
        stage('3') {
            steps {
                echo 'Hello 3'
            }
        }
    }  
}
