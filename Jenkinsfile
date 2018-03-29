pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''npm install
npm install express'''
      }
    }
    stage('Test') {
      steps {
        sh './jenkins/scripts/test.sh'
      }
    }
  }
  environment {
    CI = 'true'
  }
}