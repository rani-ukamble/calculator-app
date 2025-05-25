pipeline {
    agent any

    environment {
        AWS_ACCESS_KEY_ID = credentials('aws-access-key-id')     // Configure in Jenkins credentials
        AWS_SECRET_ACCESS_KEY = credentials('aws-secret-access-key')
        AWS_DEFAULT_REGION = 'us-east-1'
    }

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/rani-ukamble/calculator-app.git'
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                    mkdir -p /var/www/html/calculator
                    cp -r Jenkinsfile README.md index.html /var/www/html/calculator
                '''
            }
        }
    }
}
