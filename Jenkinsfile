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
                git url: 'https://github.com/Daniel202412/API-REST.git'
            }
        }
        stage('Find and Run') {
            steps {
                sh 'find ${WORKSPACE} -name mainPrueba.go' // Buscar el archivo en el repositorio
                sh 'ls -al ${WORKSPACE}/main' // Lista los archivos en la carpeta main
                sh 'go run ${WORKSPACE}/main/mainPrueba.go' // Ejecuta el archivo Go
            }
        }
    }
}
