pipeline {
    agent any

    environment {
        // मॅकच्या डॉकर बायनरीचे सर्व संभाव्य पाथ आपण इथे टाकत आहोत
        PATH = "/Applications/Docker.app/Contents/Resources/bin:/usr/local/bin:/opt/homebrew/bin:/usr/bin:/bin:/usr/sbin:/sbin"
    }

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
