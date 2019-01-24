pipeline {
  agent none
  stages {
    stage('Prepare') {
      steps {
        tool 'NodeJS-10.13.0'
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