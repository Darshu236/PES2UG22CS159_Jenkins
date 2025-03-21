pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'cd main && make'
                echo 'Build Stage Successful'
            }
        }

        stage('Test') {
            steps {
                sh 'cd main && ./hello_exec_nonexistent'  // Error: Using a non-existent executable
                echo 'Test Stage Successful'
            }
        }

        stage('Deploy') {
            steps {
                sh 'echo "Deploying application..."'
                echo 'Deployment Successful'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
