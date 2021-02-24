node {
    checkout scm 
    stage('SonarQube analysis') {
        def sonarqubeScannerHome = tool name: 'SonarQube Scanner'

        withSonarQubeEnv('SonarQubeServer') {
            bat "${sonarqubeScannerHome}/bin/sonar-scanner"
        }
    }
}