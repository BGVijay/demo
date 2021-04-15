pipeline {
  environment {
    registry = "vijaybg213/demo-test"
    registryCredential = 'dockerhub'
  }
  agent any
  stages {
    stage('Building image') {
      steps{
        script {
          docker.build registry + ":$BUILD_NUMBER"
            docker.withRegistry( registry, registryCredential ) {
        dockerImage.push()
        }
      }
    }
  }
}
}
