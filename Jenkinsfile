pipeline {
    agent {
            docker {
                image 'berkgokden/sbt-base:v0.1'
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
                sh 'echo $DOCKER_VERSION'
            }
        }
    }
}
