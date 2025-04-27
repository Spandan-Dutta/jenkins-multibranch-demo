pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo "Checking out the code..."
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo "Building from branch: ${env.BRANCH_NAME}"
            }
        }

        stage('Test') {
            steps {
                echo "Running tests..."
            }
        }
    }

    post {
        success {
            echo "Build succeeded for branch ${env.BRANCH_NAME}"
        }
        failure {
            echo "Build failed for branch ${env.BRANCH_NAME}"
        }
    }
}
