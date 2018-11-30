pipeline {
  agent any
  stages {
    stage('Build Image') {
      steps {
        sh 'docker build -t kaioaresi/jenkins_teste:${tag_img} .'
      }
    }
    stage('Push image') {
      steps {
        sh 'docker push kaioaresi/jenkins_teste:${tag_img}'
      }
    }
  }
  environment {
    tag_img = 'development'
  }
}