pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
        echo 'Build Successfull'
      }
    }
    stage('Test') {
      steps {
        sh 'bash ./jenkinsract/jenkins/scripts/test.sh'
        input(message: 'Is Test Successfull and ready to continue ?', ok: 'Yes and continue to publish and execute')
      }
    }
  }
  environment {
    HOME = '.'
    PORT_NUM = '9090'
    CI = 'true'
  }
}