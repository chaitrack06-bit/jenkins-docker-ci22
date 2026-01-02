
pipeline {
    agent any

    stages {
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
