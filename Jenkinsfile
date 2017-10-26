pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                docker run -it -v $(pwd):/src berkgokden/sbt-base:v0.1 sbt clean compile
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                docker run -it -v $(pwd):/src berkgokden/sbt-base:v0.1 sbt test
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
