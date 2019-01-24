pipeline {
  agent any
  stages {
    stage('Prepare') {
      steps {
        sh 'yarn'
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
    stage('Finish') {
      steps {
        echo 'Success'
      }
    }
  }
  tools {
    nodejs 'node'
  }
  environment {
    CI = 'true'
  }
}