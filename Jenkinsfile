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
                sh 'docker run -p 9090:8080 -p 50000:50000 jenkins/jenkins:lts'
            }
        }
    }
}
