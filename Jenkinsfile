pipeline {
    agent any

    stages {
        stage('Checkout SCM') {
            steps {
                echo 'Source code is managed by GitHub!'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building Docker Image'
                bat 'docker build -t indur-app .'
            }
        }

        stage('Test') {
            steps {
                echo 'Running Docker Container'
                bat 'docker run --rm indur-app'
            }
        }
    }
}