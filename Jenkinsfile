pipeline {
  agent any
  stages {
    stage('Test') {
      agent {
        node {
          label '10.13.0'
        }

      }
      steps {
        sh '''yarn
CI=true yarn test'''
      }
    }
  }
}