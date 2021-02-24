node {
    checkout scm 
    stage('SonarQube analysis') {
        def sonarqubeScannerHome = tool name: 'SonarQube Scanner'

        withSonarQubeEnv('SonarQubeServer') {
            sh "${sonarqubeScannerHome}/bin/sonar-scanner"
        }
    }
}