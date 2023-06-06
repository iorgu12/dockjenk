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
                    sshPut remote: remote, from: 'prog.sh', into: '/home/loco2/lab'
                    sshCommand remote: remote, command:"chmod +x /home/coco/lab/prog.sh"
                    sshCommand remote: remote, command:"systemctl start gop.service"
                    
           
                }
            }
        }
