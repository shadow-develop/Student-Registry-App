pipeline {
    agent any

    // environment {
    //     NODE_VERSION = '20' // Specify the Node.js version
    // }

    // stages {
    //     stage('Checkout Code') {
    //         steps {
    //             // Check out the code from the repository
    //             checkout scm
    //         }
    //     }

    //     stage('Install Node.js') {
    //         steps {
    //             // Install the specified Node.js version
    //             script {
    //                 // Use Node.js installation from the Jenkins tool configuration
    //                 nodejs(NODE_VERSION) {
    //                     bat 'node --version'
    //                 }
    //             }
    //         }
    //     }

        stage('Install Dependencies') {
            steps {
                // Install project dependencies
                bat 'npm install'
            }
        }

        stage('Run Tests') {
            steps {
                // Run the tests
                bat 'npm run test'
            }
        }
    }

    post {
        always {
            // Post-build actions like archiving test reports
            echo 'Cleaning up workspace'
            cleanWs()
        }
    }
