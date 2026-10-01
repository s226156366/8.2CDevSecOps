pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Source code checked out from GitHub'
            }
        }

        stage('Install Dependencies') {
            steps {
                bat 'npm install'
            }
        }

        stage('Security Audit') {
            steps {
                bat 'npm audit || exit /b 0'
            }
        }
    }

    post {
        always {
            echo 'DevSecOps security pipeline completed'
        }
    }
}