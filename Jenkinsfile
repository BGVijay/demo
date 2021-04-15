pipeline {
  environment {
    registry = 'vijaybg213/tomcat01'
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
          docker.withRegistry( registry, registryCredential ) {
        dockerImage.push()
          }
  }
}
}
    }
  }
