pipeline {
    agent any
    triggers {
        pollSCM '* * * * *'
    }
    stages {
        stage('Build') {
            steps {
                bat 'gradle assemble'
            }
        }
//          stage('Test') {
//             steps {
//                 sh 'gradlew test'
//             }
//         }
//         stage('Build Docker Image') {
//             steps {
//                 sh 'gradlew docker'
//             }
//         }
//         stage('Run Docker Image') {
//             steps {
//                 sh 'gradlew dockerRun'
//             }
//         }
    }
}