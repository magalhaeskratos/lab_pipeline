pipeline {
  agent any
  stages {
    stage('Build image') {
      steps {
        sh 'docker build -t teste/jenkins:${TAG_DEV} .'
      }
    }
    stage('Docker push') {
      steps {
        sh 'docker login -u ${DOCKER_USER} -p ${DOCKER_PASS} ; docker image push teste/jenkins:${TAG_DEV}'
      }
    }
  }
}