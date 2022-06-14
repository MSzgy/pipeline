pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
//                 sh "echo Hello Pipeline!"
                   deleteDir()
                   checkout scm
            }
        }
        stage('Test') {
            steps {
                sh "mvn verify"
            }
        }
    }
}
