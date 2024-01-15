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

  }
}