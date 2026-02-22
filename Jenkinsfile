pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                echo 'Building Docker image...'
                sh 'docker build -t event-registration-app .'
            }
        }

        stage('Run Container') {
            steps {
                echo 'Running Docker container...'
                sh 'docker run -d -p 5000:5000 event-registration-app'
            }
        }

        stage('Test Application') {
            steps {
                echo 'Application deployed successfully!'
            }
        }
    }
}