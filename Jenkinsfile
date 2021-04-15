pipeline {
  environment {
    registry = "vijaybg213/test123"
    registryCredential = 'dockerhub'
  }
  agent any
  stages {
    stage('Building image') {
      steps{
        script {
          docker.build registry + ":$BUILD_NUMBER"
            docker.withRegistry( 'vijaybg213/test123', registryCredential ) {
        dockerImage.push()
        }
      }
    }
  }
}
}
