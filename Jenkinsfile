pipeline {
  agent {
    dockerfile {
      filename 'Dockerfile'
    }

  }
  stages {
    stage('Build Image') {
      steps {
        sh 'docker build -t kaioaresi/jenkins:${tag_img} .'
      }
    }
  }
  environment {
    tag_img = 'development'
  }
}