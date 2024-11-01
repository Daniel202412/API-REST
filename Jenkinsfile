pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Daniel202412/API-REST.git'
            }
        }
        stage('Install Go') {
            steps {
                sh '''
                sudo apt-get update
                sudo apt-get install -y golang
                '''
            }
        }
        stage('Build and Run') {
            steps {
                dir('main') {
                    sh 'ls -al'
                    sh 'go env'
                    sh 'go run mainPrueba.go'
                }
            }
        }
    }
}
