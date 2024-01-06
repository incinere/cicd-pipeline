pipeline {
  agent any
  stages {
    stage('1') {
      steps {
        script {
          checkout scm
          sh 'chmod +x scripts/build.sh'

        }

      }
    }

    stage('2') {
      steps {
        script {
          sh 'scripts/build.sh'
        }

      }
    }

    stage('3') {
      steps {
        script {
          sh 'scripts/test.sh'
        }

      }
    }

    stage('4') {
      steps {
        script {
          docker.build("${registry}:${env.Build_ID}")
        }

      }
    }

    stage('5') {
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