pipeline {
    agent any

     stages {
        
stage('Run_remote') {
            steps {
                sh'chmod 400 key'
                sh 'ssh loco2@192.168.81.130 -i key -C docker run -d my-python-app'
                sh'ssh loco2@192.168.81.130 -i key -C curl http://172.17.0.2:4444/api'
                
               }
            }
        }
    }

     
