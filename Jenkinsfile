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
        stage('Install Go') {
            steps {
                sh '''
                curl -OL https://golang.org/dl/go1.16.7.linux-amd64.tar.gz
                mkdir -p ${WORKSPACE}/go
                tar -C ${WORKSPACE}/go --strip-components=1 -xzf go1.16.7.linux-amd64.tar.gz
                '''
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
