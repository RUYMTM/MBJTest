pipeline {
    agent any
    tools {
        
        maven "M3"
    }
    stages {
        stage ('Initialize') {
            steps {
                
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                
            }
        }
        stage('Build') {
            steps {
               bat 'mvn -Dmaven.test.failure.ignore=true install'
            }
        }
        stage('Test') {
            steps {
                echo 'test'
            }
            
        }
    }
}
