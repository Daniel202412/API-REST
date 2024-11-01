pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'Master', url: 'https://github.com/Daniel202412/API-REST.git'
            }
        }
        stage('Build and Run') {
            steps {
                sh 'go run mainPrueba.go'
            }
        }
    }
}
