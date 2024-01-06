pipeline {
  agent any
  stages {
    stage('2') {
      steps {
        script {
          sh 'chmod +x scripts/build.sh'
        }

      }
    }

    stage('3') {
      steps {
        script {
          sh 'scripts/build.sh'
        }

      }
    }

    stage('4') {
      steps {
        script {
          sh 'scripts/test.sh'
        }

      }
    }

  }
}