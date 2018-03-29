pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''npm install
npm install express
npm install jade
npm install socket.io'''
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