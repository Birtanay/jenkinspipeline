pipeline {
    agent any

    stages{
        stage('Build'){
            steps {
                bat 'C:\\maven\\apache-maven-3.6.0\\bin\\mvn.exe clean package'
            }
            post {
                success {
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
    }
}