pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking source code from GitHub'
            }
        }

        stage('Check Files') {
            steps {
                bat 'dir'
            }
        }

        stage('Build') {
            steps {
                bat 'echo Jenkins build successful > jenkins-build.txt'
            }
        }

        stage('Report of Build') {
            steps {
                bat 'type jenkins-build.txt'
            }
        }
    }

    post {
        success {
            echo 'Jenkins pipeline completed successfully'
        }
        failure {
            echo 'Jenkins pipeline failed'
        }
    }
}