pipeline {
    agent any
    stages {
        stage('Clone Repo') {
            steps {
                git 'https://github.com/your-username/hello-jenkins-docker.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t hello-jenkins-docker .'
            }
        }
        stage('Run Container') {
            steps {
                sh 'docker run --rm hello-jenkins-docker'
            }
        }
    }
}