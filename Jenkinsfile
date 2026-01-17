pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/rahulvaidyasdlc/Django-CI-demo-app.git'
            }
        }
        stage('Install Dependencies') {
            steps {
                bat 'python -m pip install --upgrade pip',
                bat 'pip install -r requirements.txt'

            }
        }
        stage('Run Tests') {
            steps {
                       bat 'python manage.py test'
            }
        }
    }
}