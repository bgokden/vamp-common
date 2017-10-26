pipeline {
    agent {
            docker {
                image 'berkgokden/sbt-base:v0.1'
                args '-v $WORKSPACE:/src'
            }
        }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'sbt clean compile'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh 'sbt clean test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
