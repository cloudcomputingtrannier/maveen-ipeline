pipeline {
    agent any
    tools { 
        maven 'MAVEN'
        jdk 'JDK' 
    }
    stages {
        stage ('Initialize') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                ''' 
            }
        }

        stage ('Build') {
            steps {
                echo 'This is a minimal pipeline.'
            }
        }
         post {
                success {
                    junit 'target/surefire-reports/**/*.xml' 
                }
            }
    }
}