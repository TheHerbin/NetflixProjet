pipeline {
    agent any
    tools{
        jdk 'jdk8'
        maven 'maven'
         }
    
    stages {
        stage ('Initialize') {
            steps {
                bat '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                ''' 
                }
            
            }
        }
    }
