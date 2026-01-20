pipeline {
    agent any

    stages {

        stage('Clone Repo') {
            steps {
                git credentialsId: 'github-creds',
                    url: 'https://github.com/SHIVANSHU-YADAV7/ci-cd-demo.git',
                    branch: 'main'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t cicd-app .'
            }
        }

        stage('Deploy Container') {
            steps {
                sh '''
                docker stop cicd-container || true
                docker rm cicd-container || true
                docker run -d -p 8080:80 --name cicd-container cicd-app
                '''
            }
        }
    }
}
