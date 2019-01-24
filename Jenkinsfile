pipeline {
  agent any
  stages {
    stage('Test') {
      agent {
        docker {
          image 'node:10-alpine'
        }

      }
      steps {
        sh '''npm install
CI=true npm test'''
      }
    }
  }
}