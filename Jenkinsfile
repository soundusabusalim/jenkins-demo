pipeline {
    agent any

    stages {
        stage('Get Code') {
            steps {
                echo 'Getting application from GitHub'
            }
        }

        stage('Build') {
            steps {
                sh 'ls -la'
                sh 'cat index.html'
            }
        }

        stage('Test') {
            steps {
                echo 'Application files retrieved successfully!'
            }
        }
    }
}
