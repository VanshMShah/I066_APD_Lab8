pipeline {
    agent any

    stages {

        stage('Pull from Git') {
            steps {
                git 'https://github.com/VanshMShah/I066_APD_Lab8.git'
            }
        }

        stage('Build') {
            steps {
                echo "Building the project..."
                sh 'echo Build Successful'
            }
        }

        stage('Test') {
            steps {
                echo "Running Tests..."
                sh 'echo Tests Passed'
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying Application..."
                sh 'echo Deployment Completed'
            }
        }
    }

    post {
        success {
            echo 'Pipeline executed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
