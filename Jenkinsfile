pipeline{
  agent any
  stages{
    stage('build'){
      steps{
        script{
          def scannerHome = tool name: 'SonarQubeScanner', type: 'hudson.plugins.sonar.SonarRunnerInstallation'
          withSonarQubeEnv('SonarQubeScanner') {
          sh "${scannerHome}/bin/sonar-scanner"
          }
        }
      }
    }
  }
}
