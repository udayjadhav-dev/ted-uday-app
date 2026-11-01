pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                checkout scm
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t ted-uday-app:latest .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run --rm ted-uday-app:latest'
            }
        }
    }
}

