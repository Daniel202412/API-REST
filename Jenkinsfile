pipeline {
    agent {
        label 'docker'
    }
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Daniel202412/API-REST.git'
            }
        }
        stage('Build and Run') {
            steps {
                sh 'docker run --rm -v "$PWD":/usr/src/myapp -w /usr/src/myapp golang:latest go run mainPrueba.go'
            }
        }
    }
}
