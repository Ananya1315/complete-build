pipeline {
    agent any
    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/Ananya1315/complete-build.git'
            }
        }
        stage('Maven Build') {
            steps {
                bat 'mvn clean package'
            }
        }
        stage('Docker Build') {
            steps {
                bat 'docker build -t complete-build:latest .'
            }
        }

    }
}