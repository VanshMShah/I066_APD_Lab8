pipeline {
    agent any

    stages {

        stage('Clone Kapil Repo') {
            steps {
                bat 'git clone https://github.com/kapilrahtor/Jenkins_pipeline.git'
            }
        }

        stage('Copy Files to My Repo') {
            steps {
                bat 'xcopy Jenkins_pipeline\\* . /E /H /C /I /Y'
            }
        }

        stage('Commit & Push to My Repo') {
            steps {
                withCredentials([usernamePassword(credentialsId: 'github-token', usernameVariable: 'USER', passwordVariable: 'TOKEN')]) {
                    bat 'git config user.email "jenkins@lab.com"'
                    bat 'git config user.name "Jenkins"'
                    bat 'git add .'
                    bat 'git commit -m "Auto copied files from Kapil repo" || exit 0'
                    bat 'git push https://%USER%:%TOKEN%@github.com/VanshMShah/I066_APD_Lab8.git HEAD:master'
                }
            }
        }

        stage('Build') {
            steps {
                bat 'echo Building project'
            }
        }

        stage('Test') {
            steps {
                bat 'echo Testing project'
            }
        }

        stage('Deploy') {
            steps {
                bat 'echo Deploying project'
            }
        }

    }
}
