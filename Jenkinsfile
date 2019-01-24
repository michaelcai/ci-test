pipeline {
  agent {
    docker {
      image 'node:10-alpine'
    }

  }
  stages {
    stage('Prepare') {
      steps {
        sh 'npm install'
      }
    }
    stage('Test') {
      steps {
        sh 'npm test'
      }
    }
    stage('Build') {
      steps {
        sh 'yarn build'
      }
    }
    stage('') {
      steps {
        setGitHubPullRequestStatus(state: 'SUCCESS')
      }
    }
  }
  environment {
    CI = 'true'
    HOME = '.'
  }
}