pipeline {
  agent none

  tools (nodejs 'NodeJS-10.13.0')

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
  }
  environment {
    CI = 'true'
    HOME = '.'
    npm_config_cache = 'npm-cache'
  }
}