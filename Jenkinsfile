pipeline{
  agent any
  stages{
    stage('build'){
      steps{
        withSonarQubeEnv('local_sonar') {
          sh "{tool 'sq-scanner'}/bin/sonar-scanner -Dsonar.projectKey=test01"
        }
        }//steps
  }//stage
}//stages
}//pipeline
