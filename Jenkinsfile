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

    stage('Application Build') {
      steps {
        script {
          sh 'chmod +x scripts/build.sh'
          sh 'scripts/build.sh'
        }

      }
    }

    stage('Tests') {
      steps {
        script {
          sh 'scripts/test.sh'
        }

      }
    }
 }
}
