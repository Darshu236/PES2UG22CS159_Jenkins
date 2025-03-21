pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo "Building project..."
                bat 'g++ hello.cpp -o hello_exec.exe'
            }
        }
        stage('Test') {
            steps {
                echo "Running tests..."
                bat '.\\hello_exec.exe'
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploying application..."
                bat 'copy hello_exec.exe C:\\DeploymentFolder'
            }
        }
    }

    post {
        failure {
            echo "Pipeline failed!"
        }
        success {
            echo "Pipeline executed successfully!"
        }
    }
}
