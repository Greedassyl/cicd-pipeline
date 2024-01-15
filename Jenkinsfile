pipeline {
  agent any
  stages {
    stage('build.sh') {
      steps {
        sh 'chmod +x scripts/build.sh'
        sh 'scripts/build.sh'
      }
    }

  }
}