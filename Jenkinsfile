pipeline {
    agent any
    triggers {
        pollSCM('*/5 * * * *')
    }
    stages {
        stage('Build') {
            steps {
                powershell 'mvn clean package spring-boot:repackage'
            }
        }
        stage('Test') {
            steps {
                powershell 'mvn test'
            }
        }
        
    }
}
