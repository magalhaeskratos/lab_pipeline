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
        sh '''stack_name =$(echo "$JOB_NAME" | sed \'s#/.*##g\')

echo $stack_name
'''
      }
    }
  }
  environment {
    tag_img = 'development'
  }
}