pipeline {
  agent any
  stages {
    stage('1') {
      steps {
        git(url: 'https://github.com/incinere/cicd-pipeline.git', branch: 'main', credentialsId: 'github_id')
      }
    }

  }
}