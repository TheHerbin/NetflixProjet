pipeline {
    agent any
    tools{
        jdk 'Java11'
        maven 'Maven'
         }
    
    stages {
     
        stage('Build') { 
            steps {
                bat 'mvn -B -DskipTests clean package'
            }
        }

        stage('Run') { 
            steps {
                bat returnStdout: true, script: 'java -jar  target/netflix-1.0.0.jar  netflix_titles.csv'

            }
        }
        stage('LoadWebPageIntoServer') { 
            steps {
                bat '''
                    rmdir D:\\xampp\\htdocs\\netflixprojet\\*.*
                    move C:\\ProgramData\\Jenkins\\.jenkins\\workspace\\NetflixProjet\\out\\* D:\\xampp\\htdocs\\netflixprojet
                '''

            }
        }
    }
}
