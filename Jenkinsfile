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
                echo 'build'
            }
        }
        stage('Test') {
            steps {
                echo 'test'
            }
            
        }
    }
}
