pipeline {
    agent any

    stages {

        stage('Pull from Git') {
            steps {
                echo 'Cloning the repository from GitHub...'
                git branch: 'main', url: 'https://github.com/kapilrahtor/Jenkins_pipeline.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building the project...'
                sh 'echo Build step completed'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'echo Test step completed'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                sh 'echo Deployment completed'
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
