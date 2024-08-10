pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Install Node.js and npm
                tool nodejs: '12.22.9'

                // Change directory to the project root
                dir('path/to/your/project') {
                    // Run npm install
                    sh 'npm install'
                }
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
