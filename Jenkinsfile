pipeline {
  environment {
    registry = 'vijaybg213/Helloworld'
    registryCredential = 'dockerhub'
  }
  agent any
  stages {
    stage('Building image') {
      steps{
        script {
          docker.build registry + ":$BUILD_NUMBER"
        }
      }
    }
      stage('deploy'){
        steps{
          script{
          docker.withRegistry('', registryCredential ) {
        dockerImage.push()
          }
  }
}
}
    }
  }
