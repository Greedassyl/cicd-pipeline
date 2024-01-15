pipeline {
  agent any
  stages {
    stage('build.sh') {
      steps {
        sh 'sudo apt install npm nodejs'
        sh 'chmod +x scripts/build.sh'
        sh 'scripts/build.sh'
      }
    }

  }
}