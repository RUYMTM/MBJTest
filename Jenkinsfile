pipeline {
    agent any
    tools {
        maven 'M3'
        jdk 'java_home'
    }
    stages {
        stage ('Build') {
            steps {
                bat "mvn clean verify -X" 
            }
            post {
                success {
                    junit 'target/surefire-reports/**/*.xml' 
                }
            }
        }
    }
}
