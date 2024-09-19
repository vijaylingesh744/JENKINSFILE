
pipeline {
    agent any

    stages {
        stage('Install Dependencies') {
            steps {
                // Install Node.js dependencies
                sh 'npm install --legacy-peer-deps'
            }
        }
        stage('Build') {
            steps {
                // Build the React application
                sh 'npm run build'
            }
        }

stage('Copy Files') {
            steps {
                // Make sure the destination directory exists
                sh 'mkdir -p /var/www/dev'
                // Copy the files using cp, with sudo if necessary
                sh 'sudo cp -r dist/ /var/www/dev/'
            }
        }

        stage('Deploy') {
            steps {
                // Deploy the application (this will depend on your deployment strategy)
                echo 'Deploying application...'
                // Add your deployment commands here
            }
        }
    }
    post {
        success {
            echo 'Build and deployment successful!'
        }
        failure {
            echo 'Build failed!'
        }
    }
}
