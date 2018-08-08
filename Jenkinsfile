pipeline{
  agent any
  stages{
    stage('build'){
      steps{
          sh "{tool 'sq-scanner'}/bin/sonar-scanner -X"
    }//steps
  }//stage
}//stages
}//pipeline
