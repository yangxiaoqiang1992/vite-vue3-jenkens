node {
    checkout scm 
    stages{
        stage('SonarQube analysis') {
            def sonarqubeScannerHome = tool name: 'SonarQube Scanner'

            withSonarQubeEnv('SonarQubeServer') {
                bat "${sonarqubeScannerHome}/bin/sonar-scanner"
            }
        }
        stage('Build'){
           echo "build start **********" 
        }
    }
}