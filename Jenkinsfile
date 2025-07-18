pipeline {
    agent any

    stages {
        stage('Clone GitHub Repo') {
            steps {
                git url: 'https://github.com/bmprajwal/webhosting-ec2.git', branch: 'main'
            }
        }
        stage('Deploy to Apache') {
            steps {
                sh '''
                    sudo rm -rf /var/www/html/*
                    sudo cp -r public/* /var/www/html/
                '''
            }
        }
    }
}

