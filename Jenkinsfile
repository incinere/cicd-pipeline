pipeline {
  agent any
  stages {
    stage('2') {
      steps {
        script {
          checkout scm
        }

      }
    }

    stage('3') {
      steps {
        script {
          sudo sh 'scripts/build.sh'
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

    stage('6') {
      steps {
        script {
          docker.withRegistry('','dockerhub_id'){
            docker.image("${registry}:${env.BUILD_ID}").push('latest')
            docker.image("${registry}:${env.BUILD_ID}").push("${env.BUILD_ID}")
          }
        }

      }
    }

  }
  environment {
    registry = 'incinere/test'
  }
}