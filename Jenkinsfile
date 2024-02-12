pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                git 'https://github.com/issath98/Django-Check-Jenkins.git'
                sh 'docker build -t simple-django-app .'
            }
        }

        stage('Test') {
            steps {
                // Add test steps here if needed
            }
        }

        stage('Deploy') {
            steps {
                sh 'docker run -d -p 8000:8000 simple-django-app'
            }
        }
    }
}
