pipeline {
    agent any
    tools{
        jdk 'JDK8'
        maven 'Maven'
         }
    
    stages {
     
    stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package'
                }
            }
        
    stage('Run') { 
            steps {
                sh returnStdout: true, script: 'java -jar  netflix-1.0.0.jar  ../netflix_titles.csv'
            
                }
            }
        }
    }
