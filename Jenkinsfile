pipeline {
    agent any

    stages {

        stage('Install') {
            steps {
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                sh 'npm test'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t ci-cd-demo:1 .'
            }
        }

        stage('List Images') {
            steps {
                sh 'docker images'
            }
        }
    }
}
