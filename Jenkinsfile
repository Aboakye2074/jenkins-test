pipeline {
    // Define the agent where the pipeline will run. 'any' means it can run on any available agent.
    agent any

    stages {
        // First stage: Build
        stage('Build') {
            steps {
                echo 'Building...'
            }
        }
        
        // Second stage: Test
        stage('Test') {
            steps {
                echo 'testing...'
            }
        }

        // Third stage: Deploy
        stage('Deploy') {
            steps {
                script {
                    // Conditional deployment based on the branch name.
                    // If the current branch is 'master', deploy to production.
                    if (env.BRANCH_NAME == 'master') {
                        echo 'Deploying to production...'
                        // Add production deployment steps here.
                    } else {
                        // If the branch is not 'master', deploy to staging.
                        echo 'Deploying to staging...'
                        // Add staging deployment steps here.
                    }
                }
            }
        }
    }
}
