pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        git(url: 'https://github.com/balu9493/exp-project', branch: 'main')
      }
    }

    stage('list dir') {
      steps {
        bat 'dir'
      }
    }

    stage('Unit tests') {
      steps {
        bat 'npm install & npm test'
      }
    }

  }
}