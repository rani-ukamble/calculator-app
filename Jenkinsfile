pipeline {
    agent any

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
