pipeline {
  agent any
  stages {
    stage('Build Image') {
      steps {
        sh '''#docker build -t kaioaresi/jenkins_teste:${tag_img} .

docker --version'''
      }
    }
  }
  environment {
    tag_img = 'development'
  }
}