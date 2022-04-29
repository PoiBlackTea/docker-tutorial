pipeline {
    agent any
    stages {
        stage('verify tooling'){
            steps{
                sh '''
                    docker version
                    docker info
                '''
            }
        }
        stage('Build'){
            steps{
                sh '''
                    docker-compose build
                    docker-compose up
                '''
            }
        }
        stage('Kill'){
            steps{
                sh "docker-compose down"
            }
        }
    }
}