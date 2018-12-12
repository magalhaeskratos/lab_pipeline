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
        sh 'docker stack deploy -c docker-compose.yml jenkins_pipeline'
      }
    }
  }
  environment {
    NAME_IMG = 'jenkins'
  }
}