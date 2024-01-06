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

    stage('5') {
      steps {
        script {
          docker.build("${registry}:${env.Build_ID}")
        }

      }
    }

  }
  environment {
    registry = 'incinere/test'
  }
}