pipeline {
  agent {
    dockerfile {
      filename 'Dockerfile'
    }

  }
  stages {
    stage('Build Image') {
      steps {
        sh 'docker --version'
      }
    }
  }
  environment {
    tag_img = 'development'
  }
}