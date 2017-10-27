pipeline {
    agent {
            docker {
                image 'berkgokden/sbt-base:v0.1'
                args '-v /var/run/docker.sock:/var/run/docker.sock'
            }
        }

    stages {
        stage('Build') {
            steps {
                sh 'sbt clean compile'
            }
        }
        stage('Test') {
            steps {
                sh 'sbt clean test'
            }
        }
        stage('Deploy') {
            steps {
                sh 'docker ps'
            }
        }
    }
}
