pipeline {
    agent any  // This means Jenkins will run this pipeline on any available agent

    environment {
        // Optional: Define environment variables, if needed
        // MY_VARIABLE = 'value'
    }

    stages {
        // Stage 1: Checkout code from Git repository
        stage('Checkout') {
            steps {
                echo 'Checking out code from Git...'
                // This fetches the code from the specified Git repository and branch
                git url: 'https://github.com/youruser/yourrepo.git', branch: 'main'
            }
        }

        // Stage 2: Build the project
        stage('Build') {
            steps {
                echo 'Building the project...'
                // Replace this with your actual build command, e.g., `mvn clean install` or `npm install`
                sh 'echo "Build successful!"' 
            }
        }

        // Stage 3: Run tests
        stage('Test') {
            steps {
                echo 'Running tests...'
                // Replace with your test command (e.g., `mvn test` or `npm test`)
                sh 'echo "Running tests..."'  // Replace with your actual test command
            }
        }

        // Stage 4: Deploy
        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                // Replace with your actual deployment commands, such as Docker deploy, AWS deploy, etc.
                sh 'echo "Deploying application..."' 
            }
        }
    }

    post {
        // This block runs after the stages above
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
        always {
            echo 'This will always run, regardless of success or failure.'
        }
    }
}
