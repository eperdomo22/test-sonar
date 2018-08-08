pipeline{
  agent any
  stages{
    stage('build'){
      steps{
        script{
          def scanner = tool 'sq-scanner'
          withSonarQubeEnv('local_sonar') {
          sh "${scanner}/bin/sonar-scanner -Dsonar.projectKey=test01"
          }
        }
        }//steps
  }//stage
    stage("Quality Gate") {
            steps {
               withSonarQubeEnv('local_sonar') {
              timeout(time: 1, unit: 'MINUTES') {
                waitForQualityGate abortPipeline: true
              }
               }
            }
          }
}//stages
}//pipeline
