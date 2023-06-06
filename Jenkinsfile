pipeline {
    agent any

    stages {
        
stage('Deploy') {
            steps {
                script {
                    def remote = [:]
                    remote.name = 'my-ssh-server'
                    remote.host = '192.168.81.130'
                    remote.user = 'loco2'
                    remote.password = 'loco12'  
                    remote.allowAnyHosts = true   
                    echo 'Deploying....'
                    sshCommand remote: remote, command:"docker run -d -p 9090:80 --name server1 nginx:1.0"
                    sshCommand remote: remote, command:"docker ps"
                    
           
                }
            }
        }
    }
}
