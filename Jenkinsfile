pipeline {
    agent any
    environment {
        GOROOT = "${env.WORKSPACE}/go"
        GOPATH = "${env.WORKSPACE}/gopath"
        PATH = "${env.PATH}:${env.GOROOT}/bin:${env.GOPATH}/bin"
    }
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Daniel202412/API-REST.git'
            }
        }
        stage('Build and Run') {
            steps {
                sh 'find . -name mainPrueba.go' // Busca el archivo en el repositorio
                sh 'go run main/mainPrueba.go' // Ejecuta el archivo desde la carpeta main
            }
        }
    }
}
