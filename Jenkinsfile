pipeline {
    environment {
    PATH = "C:\\Program Files\\Git\\usr\\bin; C:\\Program Files\\Git\\bin;${env.PATH}"
    agent any
    stages{
        stage('Build'){
            steps {
                bat 'mvn clean package'
            }
            post {
                success{
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
    }
}
