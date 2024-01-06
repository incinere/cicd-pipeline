pipeline {
  agent any
  stages {
    stage('1') {
      steps {
        git(url: 'https://github.com/incinere/cicd-pipeline/edit/main/Jenkinsfile', branch: 'main', credentialsId: 'github_id')
      }
    }

  }
}