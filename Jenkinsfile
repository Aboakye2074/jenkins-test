pipeline {
    // Define the agent where the pipeline will run. 'any' means it can run on any available agent.
    agent any

    // stages of the pipeline
    stages {
        // First stage: Build
        stage('Build') {
            steps {
                
                echo 'Building...'
            }
        }

        // Second stage: Test
        stage('Test') {
            // Run multiple stages in parallel to save time.
            parallel {
                // Sub-stage for unit tests
                stage('Unit Tests') {
                    steps {
                        // a message indicate that unit tests are running.
                        echo 'Running unit tests...'
                        // Add steps to run unit tests here.
                    }
                }
                // Sub-stage for integration tests
                stage('Integration Tests') {
                    steps {
                        // message to indicate that integration tests are running.
                        echo 'Running integration tests...'
                        // Add steps to run integration tests here.
                    }
                }
            }
        }

        // Third stage: Deploy
        stage('Deploy') {
            steps {
                // message to indicate that the deployment process is starting.
                echo 'Deploying...'
                // Add deployment steps here, such as deploying to a server, updating a database, etc.
            }
        }
    }
}
