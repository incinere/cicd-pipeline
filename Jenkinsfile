pipeline {
  agent any
  stages {
    stage('1') {
      steps {
        echo 'hello'
      }
    }

    stage('2') {
      steps {
        sh '/scripts/build.sh'
      }
    }

  }
}