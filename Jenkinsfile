pipeline {
  agent any
  stages {
    stage('Checkout code') {
      steps {
        git(url: 'https://github.com/TaraGithub/new-repo', branch: 'main', credentialsId: 'GithubCred')
      }
    }

    stage('log') {
      parallel {
        stage('log') {
          steps {
            sh 'ls -la'
          }
        }

        stage('Front-end unit test') {
          steps {
            sh 'cd front-end && npm i && npm run test:unit'
          }
        }

      }
    }

  }
}