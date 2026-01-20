pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo "Build started..."
                sh 'ls -la'
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                echo "Deploying application..."
                sudo rm -rf /var/www/html/*
                sudo cp -r . /var/www/html/
                '''
            }
        }

    }
}