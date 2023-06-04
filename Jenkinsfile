pipeline {
    agent any
 

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/iorgu12/dockjenk.git'
            }
        }
        
        stage('Test') {
            steps {
                bat 'go test'
            }
        }
        

        stage('Build') {
            steps {
                bat 'go build -o prog.exe prog.go'
            }
        }
        

    }
}
