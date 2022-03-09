pipeline {
    agent any
    tools{
        jdk 'JDK8'
        maven 'Maven'
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
        stage('Build') { 
            steps {
                sh 'mvn clean package'
                echo 'build'
            
                }
            }
        }
    }
