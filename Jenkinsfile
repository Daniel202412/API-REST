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
                dir('main') { // Apunta a la carpeta main
                    sh 'ls -al' // Lista los archivos en la carpeta main para verificar
                    sh 'go run mainPrueba.go'
                }
            }
        }
    }
}
