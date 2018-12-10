pipeline {
  agent any
  stages {
    stage('Built image') {
      steps {
        sh 'docker build -t teste/jenkins:${TAG_DEV} .'
      }
    }
  }
}