pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''npm install
npm install express
npm install jade
npm install socket.io
npm install yargs'''
      }
    }
    stage('Startup App') {
      steps {
        sh '''npm start
'''
      }
    }
    stage('Test App') {
      steps {
        sh 'start chrome.exe http://localhost:8081'
      }
    }
  }
  environment {
    CI = 'true'
  }
}