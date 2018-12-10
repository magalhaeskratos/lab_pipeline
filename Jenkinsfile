pipeline {
  agent any
  stages {
    stage('Built image') {
      steps {
        sh 'docker built -t teste/jenkins:${TAG_DEV} .'
      }
    }
  }
}