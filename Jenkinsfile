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
        sh 'runas /user:peter /savedcred "C:\\Program Files (x86)\\Google\\Chrome\\Application\\chrome.exe" "http://localhost:8081"'
      }
    }
    stage('Deliver') {
      steps {
        input 'Finished using the web site? (Click "Proceed" to continue)'
      }
    }
  }
  environment {
    CI = 'true'
  }
}