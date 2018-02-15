pipeline{
  agent any
  stages{
    stage('build'){
      steps{
        script{
          def scannerHome = tool name: 'SonarQubeScanner'
          
          sh "${scannerHome}/bin/sonar-scanner -Dsonar.projectKey=test2   -Dsonar.sources=.   -Dsonar.host.url=http://172.16.10.80:9000   -Dsonar.login=e4df15f48df1fcf40bd1e948dfe121422d0e975a"
        }
      }
    }
  }
}
