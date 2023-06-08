pipeline {
    agent any

     stages {
        
stage('Run_remote') {
            steps {
                sh 'ssh loco2@192.168.81.130 -i key -C docker run -d my-python-app'
                sh'docker run -d my-python-app'
                sh'curl http://172.17.0.2:4444/api'
                
               }
            }
        }
    }

     
