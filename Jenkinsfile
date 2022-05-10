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
        
        steps {
          sshagent(credentials: ['webfiles']) {
            sh '''
                [ -d ~/.ssh ] || mkdir ~/.ssh && chmod 0700 ~/.ssh
                ssh-keyscan -t rsa,dsa example.com >> ~/.ssh/known_hosts
                ssh user@example.com ...
            '''
          }
      }
    
  
        stage('3') {
            steps {
                echo 'Hello 3'
            }
        }
    }  
}
