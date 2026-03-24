pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking source code'
            }
        }

        stage('Check Files') {
            steps {
                bat 'dir'
            }
        }

        stage('Build Report') {
            steps {
                bat 'echo Build triggered automatically from GitHub change > build-report.txt'
                bat 'type build-report.txt'
            }
        }
    }

    post {
        success {
            echo 'Automatic build completed successfully'
        }
        failure {
            echo 'Automatic build failed'
        }
    }
}