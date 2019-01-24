pipeline {
  agent {
    docker {
      image 'node:10-alpine'
    }

  }
  stages {
    stage('Prepare') {
      steps {
        sh '''npm i -g yarn
yarn'''
      }
    }
    stage('Test') {
      steps {
        sh 'yarn test'
      }
    }
    stage('Build') {
      steps {
        sh 'yarn build'
      }
    }
  }
  environment {
    CI = 'true'
    HOME = '.'
  }
}