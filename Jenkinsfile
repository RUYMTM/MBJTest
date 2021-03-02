pipeline {
    agent any
    tools {
        maven 'M3'
        jdk 'java_home'
    }
    stages {
        stage ('Build') {
            steps {
                bat "cd SimpleTest"
                bat "mvn clean verify" 
            }
            post {
                success {
                    junit 'target/surefire-reports/**/*.xml' 
                }
            }
        }
    }
}
