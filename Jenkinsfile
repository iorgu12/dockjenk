pipeline {
    agent any

     stages {
        
stage('Run_remote') {
            steps {
                sh 'ssh -o StrictHostKeyChecking=no -v -i /home/loco3/key loco2@192.168.81.130'
                sh'docker run -d my-python-app'
                sh'curl http://172.17.0.2:4444/api'
                
               }
            }
        }
    }

     
