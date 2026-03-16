pipeline {
    agent any

    stages {

        stage('Pull from Git') {
            steps {
                echo 'Cloning Kapil repository...'
                git branch: 'main', url: 'https://github.com/kapilrahtor/Jenkins_pipeline.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building the project...'
                bat 'echo Build stage completed'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing the project...'
                bat 'echo Test stage completed'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the project...'
                bat 'echo Deployment completed'
            }
        }

    }

    post {
        success {
            echo 'Pipeline executed successfully'
        }
        failure {
            echo 'Pipeline failed'
        }
    }
}
