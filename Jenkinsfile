pipeline {
  agent {
    docker {
      image 'jenkins/jenkins:2.150'
      args '''COPY plugins.txt /usr/share/jenkins/ref/plugins.txt
RUN /usr/local/bin/install-plugins.sh < /usr/share/jenkins/ref/plugins.txt'''
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