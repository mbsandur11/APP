pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from the GitHub repository
                checkout scm
            }
        }

        stage('Install Dependencies') {
            steps {
                // Install project dependencies using npm
                sh 'npm install'
            }
        }

        stage('Build Project') {
            steps {
                // Build the project using npm
                sh 'npm run build'
            }
        }

        // Add more stages as needed, such as testing or deployment stages

    }

    post {
        always {
            // Clean up workspace or perform other post-build actions
            cleanWs()
        }
    }
}
