pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                // Ensure the branch name matches (main or master)
                git branch: 'main', url: 'https://github.com/rahulvaidyasdlc/Django-CI-demo-app.git'
            }
        }
        stage('Install Dependencies') {
            steps {
                // Removed the comma from the end of the next line
                bat 'python -m pip install --upgrade pip'
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
