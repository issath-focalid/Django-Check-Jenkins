pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                // Clone the repository
                git 'https://github.com/issath98/Django-Check-Jenkins.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                // Build the Docker image
                script {
                    docker.build('django-app:latest', '.')
                }
            }
        }

        stage('Deploy Docker Container') {
            steps {
                // Deploy the Docker container
                script {
                    docker.image('django-app:latest').run('-p 8000:8000')
                }
            }
        }
    }
}
