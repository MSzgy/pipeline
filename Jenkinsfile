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
                export MAVEN_HOME=/var/jenkins_home/maven
                export PATH=$PATH:$MAVEN_HOME/bin
                sh "mvn --version"
                sh "mvn clean package"
                sh "mvn verify"
            }
        }
    }
}
