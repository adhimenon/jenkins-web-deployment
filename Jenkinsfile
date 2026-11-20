pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out source code from GitHub'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building the web application'
            }
        }

        stage('Deploy') {
            steps {
                sh 'cp index.html /var/www/html/index.html'
                echo 'Website deployed successfully'
            }
        }

        stage('Verify') {
            steps {
                sh 'curl -f http://localhost/'
                echo 'Website verification completed'
            }
        }
    }
}
