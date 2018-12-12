pipeline {
  agent any
  stages {
    stage('Build image') {
      steps {
        sh 'docker build -t kaioaresi/${NAME_IMG}:${TAG_DEV} .'
      }
    }
    stage('Deploy') {
      steps {
        sh 'cat docker-compose.yml'
      }
    }
  }
  environment {
    NAME_IMG = 'jenkins'
  }
}