pipeline {
    agent any
    
    stages {
         stage('Run Sonarqube') {
             environment {
                 scannerHome = tool 'sonar-scanner'
             }
             steps {
                 withSonarQubeEnv(credentialsId: 'sonar-token', installationName: 'sonar-server') {
                     sh "${scannerHome}/bin/sonar-scanner"
                 }
             }
         }

    }
}
