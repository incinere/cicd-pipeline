pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'script scripts/build.sh'
      }
    }

    stage('test') {
      steps {
        sh 'script scripts/test.sh'
      }
    }

    stage('docker') {
      steps {
        script {
          docker build -t test
        }

      }
    }

    stage('image') {
      steps {
        script {
          docker image push incinere/test
        }

      }
    }

  }
}