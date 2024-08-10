pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps{
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/oaleev/todo-list.git']])
            }
        }
        stage('Test') {
            steps {
                // Run unit tests with Jest (assuming you have a jest.config.js file)
                sh 'npm test'
            }
        }

        stage('Deploy') {
            steps {
                // Deploy the application to your production environment (e.g., via SSH or a deployment script)
                sh 'npm run deploy'
            }
        }
    }
}
