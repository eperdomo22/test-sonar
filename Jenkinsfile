pipeline{
  agent any
  stages{
    stage('build'){
      steps{
        withSonarQubeEnv('local_sonar'){
          sh "{tool 'sq-scanner'}/bin/sonar-scanner"
      }//with
    }//steps
  }//stage
}//stages
}//pipeline
