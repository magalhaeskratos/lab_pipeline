pipeline {
  agent any
  stages {
    stage('Build Image') {
      steps {
        sh 'docker --version'
      }
    }
  }
  environment {
    tag_img = 'development'
  }
}