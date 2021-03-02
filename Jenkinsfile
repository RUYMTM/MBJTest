pipeline {
    agent any
    tools {
        maven 'M3'
        jdk 'java_home'
    }
    stages {
        stage ('Build') {
            steps {
                bat "mvn clean --file *.pom" 
            }
            post {
                success {
                    junit 'target/surefire-reports/**/*.xml' 
                }
            }
        }
    }
}
