pipeline {
  agent any
  stages {
    stage('Test') {
      steps {
        sh 'CI=true npm test'
      }
    }
  }
}