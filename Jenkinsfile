pipeline {
    agent any

     stages {
        
stage('Run_remote') {
            steps {
                script {
                    def remote = [:]
                    remote.name = 'my-ssh-server'
                    remote.host = '192.168.81.130'
                    remote.user = 'loco2'
                    remote.password = 'loco12'  
                    remote.allowAnyHosts = true   
                    echo 'Deploying....'
                    sshCommand remote: remote, command:"docker run my-python-app"
                    sshCommand remote: remote, command:"docker ps"
                    sshCommand remote: remote, command:"echo 'Health checking....'"
                    sshCommand remote: remote, command:"curl http://172.17.0.2:4444/api"
                    sshCommand remote: remote, command:"echo 'Application is up and running.'"
                    
           
                }
                script {
                    def remote = [:]
                    remote.name = 'my-ssh-server'
                    remote.host = '192.168.81.130'
                    remote.user = 'loco2'
                    remote.password = 'loco12'  
                    remote.allowAnyHosts = true   
                    echo 'Deploying....'
                    sshCommand remote: remote, command:"curl http://172.17.0.2:4444/api"
                    sshCommand remote: remote, command:"echo 'Application is up and running.'"
                }
               }
            }
        }
    }

     
