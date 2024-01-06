pipeline {
  agent any
  stages {
    stage('Git checkout') {
      steps {
        script {
          checkout scm
        }

      }
    }

    stage('2') {
      steps {
        script {
          sh 'chmod +x scripts/build.sh'          sh 'scripts/build.sh'
        }

      }
    }

  }
}