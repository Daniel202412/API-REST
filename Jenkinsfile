pipeline {
    agent {
        docker {
            image 'golang:latest'
            args '-v /var/run/docker.sock:/var/run/docker.sock -v $HOME:$HOME'
        }
    }
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Daniel202412/API-REST.git'
            }
        }
        stage('Build and Run') {
            steps {
                sh 'go run mainPrueba.go'
            }
        }
    }
}
