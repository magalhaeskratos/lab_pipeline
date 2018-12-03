pipeline {
  agent any
  stages {
    stage('Build Image') {
      steps {
        sh 'docker build -t kaioaresi/jenkins_teste:${tag_img} .'
      }
    }
    stage('Stack update') {
      steps {
        sh 'echo $JOB_NAME'
      }
    }
  }
  environment {
    tag_img = 'development'
  }
}