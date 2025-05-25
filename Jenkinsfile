pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/rani-ukamble/calculator-app.git'
            }
        }

        stage('Deploy') {
            steps {
                // Replace with your actual deployment path
                sh 'cp -r * /var/www/html/calculator'
            }
        }
    }
}
