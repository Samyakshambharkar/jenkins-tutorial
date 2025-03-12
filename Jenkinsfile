pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out code from GitHub...'
                checkout scm
            }
        }
        stage('Build') {
            steps {
                echo 'Building...'
                // Add any build steps here (e.g., linting, testing)
            }
        }
        stage('Deploy') {
            steps {
                echo 'Running deployment steps...'
                // Add deployment steps here (e.g., file validation)
                sh 'cat index.html' // Verify the file content
            }
        }
    }
    post {
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
