pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                echo 'Repository cloned'
            }
        }

        stage('Build') {
            steps {
                echo 'Build successful'
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                sudo rm -rf /var/www/html/*
                sudo cp index.html /var/www/html/
                '''
            }
        }
    }
}