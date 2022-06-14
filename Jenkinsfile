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
                sh "export HOME=/var/jenkins_home/maven"
                sh "export PATH=$PATH:$HOME/bin"
                sh "mvn --version"
                sh "mvn clean package"

                sh "mvn verify"
            }
        }
    }
}
