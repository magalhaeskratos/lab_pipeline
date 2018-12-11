pipeline {
  agent any
  stages {
    stage('Build image') {
      steps {
        sh 'docker build -t kaioaresi/${NAME_IMG}:${TAG_DEV} .'
      }
    }
    stage('Docker push') {
      steps {
        sh 'docker login -u ${DOCKER_USER} -p ${DOCKER_PASS} ; docker image push kaioaresi/${NAME_IMG}:${TAG_DEV}'
      }
    }
  }
  environment {
    NAME_IMG = 'jenkins'
  }
}