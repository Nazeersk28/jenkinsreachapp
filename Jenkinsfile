pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
        echo 'Build Successfull'
      }
    }
  }
  environment {
    Home = '.'
    PORT_NUM = '9090'
    CI = 'true'
  }
}