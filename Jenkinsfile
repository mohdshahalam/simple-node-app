pipeline {
    agent any

    stages {
        stage('Clone repository') {
            steps {
                // Clone your repository
                git 'https://github.com/mohd-shahalam/simple-node-app.git'
            }
        }
        stage('Build') {
            steps {
                // Run a simple build step
                sh 'echo "Building project..."'
            }
        }
        stage('Test') {
            steps {
                // Run tests (you can add your testing scripts)
                sh 'echo "Running tests..."'
            }
        }
        stage('Deploy') {
            steps {
                // Deploy application (mock step for now)
                sh 'echo "Deploying application..."'
            }
        }
    }

    post {
        always {
            // Archive build artifacts, logs, etc.
            archiveArtifacts artifacts: '**/target/*.jar', allowEmptyArchive: true
            // Send notifications (e.g., email or Slack)
        }
        success {
            echo 'Pipeline succeeded'
        }
        failure {
            echo 'Pipeline failed'
        }
    }
}

