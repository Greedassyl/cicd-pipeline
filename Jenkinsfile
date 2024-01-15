pipeline {
  agent any
  stages {
    stage('build.sh') {
      steps {
        sh 'sudo apt install npm nodejs -y'
        sh 'chmod +x scripts/build.sh'
        sh 'scripts/build.sh'
      }
    }

    stage('test.sh') {
      steps {
        sh 'chmod +x scripts/test.sh'
        sh 'scripts/test.sh'
      }
    }

    stage('docker build and push') {
      steps {
        sh 'sudo docker build -t asyl13/ci-cd-epam-training:1 .'
        sh 'sudo docker login -u $DOCKER_LOGIN -p $DOCKER_PASS'
        sh 'sudo docker push asyl13/ci-cd-epam-training:1'
      }
    }

  }
}