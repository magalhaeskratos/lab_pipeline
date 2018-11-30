pipeline {
  agent any
  stages {
    stage('Build Image') {
      steps {
        sh 'docker build -t kaioaresi/jenkins_teste:${tag_img} .'
      }
    }
    stage('Up stack') {
      steps {
        sh 'docker container run -d -p 8080:8080 kaioaresi/jenkins_teste:${tag_img}'
      }
    }
  }
  environment {
    tag_img = 'development'
  }
}