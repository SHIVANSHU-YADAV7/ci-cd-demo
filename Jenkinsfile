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
        sudo cp -r * /var/www/html/
        '''
    }
}
    }
}
