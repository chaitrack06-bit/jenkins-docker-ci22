pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/chaitrack06-bit/jenkins-docker-ci22.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t jenkins-ci-demo:latest .'
            }
        }

        stage('Run Docker Image') {
            steps {
                sh 'docker run --rm jenkins-ci-demo:latest'
            }
        }
    }
}
