pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                //sh 'npm install'
                sh 'apt-get install homebridge'
            }
        }

        stage('Deploy') {
            steps {
                //sh 'npm run'
                sh 'systemctl start homebridge'
            }
        }
    }

    post {
        success {
            echo 'Deployment successfull!'
        }
        failure {
            echo 'Deployment failed!'
        }
    }
}
