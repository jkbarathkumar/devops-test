pipeline {
    agent any

    environment {
        IMAGE_NAME = 'barathkumar29/simple-java-maven-app'
        IMAGE_TAG = 'latest'
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build & Test') {
            steps {
                echo 'Building and testing the Maven app...'
                sh 'mvn clean install'
            }
        }

       

            }
        }
    

    post {
        always {
            echo 'Pipeline finished.'
        }
        success {
            echo 'Pipeline Success.'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}
