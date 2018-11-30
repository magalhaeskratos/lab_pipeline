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
        sh 'docker login --username ${docker_user} --password-stdin ${docker_pass}'
        sh 'docker push kaioaresi/jenkins_teste:${tag_img}'
      }
    }
  }
  environment {
    tag_img = 'development'
  }
}