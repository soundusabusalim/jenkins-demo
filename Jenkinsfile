pipeline {
    agent any

    stages {
        stage('Get Code') {
            steps {
                echo 'Getting application from GitHub'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t jenkins-demo-web:2.0 .'
            }
        }

        stage('Deploy') {
            steps {
                sh 'docker rm -f jenkins-demo-web || true'
                sh 'docker run -d --name jenkins-demo-web -p 8086:80 jenkins-demo-web:2.0'
            }
        }
    }
}
