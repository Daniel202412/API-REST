pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Daniel202412/API-REST.git'
            }
        }
        stage('Install Go') {
            steps {
                sh '''
                apt-get update
                apt-get install -y golang
                '''
            }
        }
        stage('Build and Run') {
            steps {
                sh 'go run mainPrueba.go'
            }
        }
    }
}
