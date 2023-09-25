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
                sh 'npm install'
                //sh 'sudo apt-get install homebridge'
            }
        }

        stage('Deploy') {
            steps {
                sh 'npm run'
                //sh 'sudo systemctl start homebridge'
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
