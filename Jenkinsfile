pipeline {
    agent any
    stages {
        stage('Clone Repo') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/Yuvrajdevelopers/hello-jenkins-docker.git',
                    credentialsId: '8659114a-2c97-4f59-a460-a6ed55772d8f'
            }
        }
        stage('Build Docker Image') {
            steps {
                bat 'docker build -t hello-jenkins-docker .'
            }
        }
        stage('Run Container') {
            steps {
                bat 'docker run --rm hello-jenkins-docker'
            }
        }
    }
}
