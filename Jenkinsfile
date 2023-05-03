pipeline {
    agent any
    triggers {
        pollSCM '* * * * *'
    }
    stages {
        stage('Build') {
            steps {
                bat '.\\gradlew assemble'
            }
        }
         stage('Test') {
            steps {
                bat '.\\gradlew test'
            }
        }
        stage('Build Docker Image') {
            steps {
                bat '.\\gradlew docker'
            }
        }
        stage('Run Docker Image') {
            steps {
                bat '.\\gradlew dockerRun'
            }
        }
    }
}