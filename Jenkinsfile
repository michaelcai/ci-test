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
        setGitHubPullRequestStatus(state: 'SUCCESS', message: 'Complete', context: 'jobContext')
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