pipeline {
    agent any
    stages {
        stage('Run Jenkins Docker Container') {
            steps {
                sh '''
                docker run -d --name jenkins_server -p 9090:8080 -p 50000:50000 jenkins/jenkins:lts
                '''
            }
        }
    }
}
