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
                // Intentar instalar Go sin necesidad de sudo
                sh '''
                curl -OL https://golang.org/dl/go1.16.7.linux-amd64.tar.gz
                tar -C /usr/local -xzf go1.16.7.linux-amd64.tar.gz
                export PATH=$PATH:/usr/local/go/bin
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

