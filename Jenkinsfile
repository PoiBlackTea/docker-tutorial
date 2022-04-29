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
                    cd ~/jenkins
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