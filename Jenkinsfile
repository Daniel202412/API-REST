pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Daniel202412/API-REST.git'
            }
        }
        stage('Verify and Run') {
            steps {
                dir('main') {
                    sh 'ls -al' // Lista los archivos en la carpeta main para verificar
                    sh 'go env' // Verifica la configuración de Go
                    sh 'go run mainPrueba.go' // Ejecuta el archivo Go
                }
            }
        }
    }
}
