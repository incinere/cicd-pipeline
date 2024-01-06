pipeline {
  agent any
  stages {
    stage('2') {
      steps {
        sh './scripts/build.sh'
      }
    }

    stage('3') {
      steps {
        sh './scripts/test.sh'
      }
    }

  }
}