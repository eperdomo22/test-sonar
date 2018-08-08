pipeline{
  agent any
  stages{
    stage('build'){
      steps{
          sh "{tool 'sq-scanner'}/bin/sonar-scanner"
    }//steps
  }//stage
}//stages
}//pipeline
