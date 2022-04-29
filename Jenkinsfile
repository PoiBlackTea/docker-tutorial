pipeline {
    agent any
    stages {
        stage('verify tooling'){
            steps{
                sh 'docker version'
                sh 'docker info'
            }
        }
        stage('Build'){
            steps{
                sh 'cd ~/jenkins'
                sh 'docker-compose build'
                sh 'docker-compose up'
            }
        }
        stage('Kill'){
            steps{
                sh "docker-compose down"
            }
        }
    }
}