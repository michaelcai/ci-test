pipeline {
  agent any
  stages {
    stage('Test') {
      agent {
        docker {
          image 'node:10-alpine'
          args '-p 3000:3000'
        }

      }
      steps {
        sh '''npm install
CI=true npm test'''
      }
    }
  }
}