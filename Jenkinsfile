pipeline {
    agent any
    stages{

        stage('Install Dependencies') {
            steps {
                // Install project dependencies
                bat 'npm install'
            }
        }

        stage('Run Tests') {
            steps {
                // Run the tests
                bat 'npm test'
            }
        }
    }
}