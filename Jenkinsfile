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
                    sshCommand remote: remote, command:"docker run -d -p 9090:80 --name server2 nginx:1.0"
                    sshCommand remote: remote, command:"docker ps"
                    sshCommand remote: remote, command:"echo 'Health checking....'"
                    sshCommand remote: remote, command:"httpRequest(url: "http://192.168.81.130:9090")"
                    sshCommand remote: remote, command:"echo 'Application is up and running.'"
                    
           
                }
            }
        }
    }
}
