pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Retrieving source code'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building Docker Image'
                bat 'docker build -t indur-app .'
            }
        }

    }
}