pipeline {
  environment {
    registry = 'vijaybg213/images'
    registryCredential = 'dockerhub'
  }
  agent any
  stages {
    stage('Building image') {
      steps{
        script {
          docker.build registry + ":$BUILD_NUMBER"
            docker.withRegistry( 'vijaybg213/images', registryCredential ) {
        dockerImage.push()
        }
      }
    }
  }
}
}
