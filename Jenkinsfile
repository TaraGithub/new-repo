pipeline {
  agent any
  stages {
    stage('Checkout code') {
      steps {
        git(url: 'https://github.com/TaraGithub/new-repo', branch: 'main', credentialsId: 'GithubCred')
      }
    }

    stage('log') {
      steps {
        sh 'ls -la'
      }
    }

  }
}