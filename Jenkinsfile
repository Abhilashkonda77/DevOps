pipeline {
    agent any  // Runs on any available agent

    environment {
        // Define environment variables if needed
        MY_VAR = 'value'
    }

    stages {
        stage('Build') {
            steps {
                // Run build commands here, for example:
                echo 'Building the project...'
                script {
                    def test = (2 + 2) > 3 ? 'cool' : 'not cool'
                    echo test
                }
                // sh './build.sh'  // Replace with your actual build command
            }
        }

        stage('Test') {
            steps {
                // Run tests here, for example:
                echo 'Running tests...'
                // sh './run_tests.sh'  // Replace with your actual test command
            }
        }

        stage('Deploy') {
            steps {
                // Deploy your application, for example:
                echo 'Deploying the application...'
                // sh './deploy.sh'  // Replace with your actual deploy command
            }
        }
    }

    post {
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed.'
        }
        always {
            echo 'Cleaning up resources...'
            // Perform cleanup tasks if needed
        }
    }
}
