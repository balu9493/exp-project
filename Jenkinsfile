pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        git(url: 'https://github.com/balu9493/exp-project', branch: 'main')
      }
    }

    stage('list dir') {
      parallel {
        stage('list dir') {
          steps {
            bat 'dir'
          }
        }

        stage('Unit tests') {
          steps {
            powershell 'nuget restore exp-project; msbuild exp-project.sln;  Invoke-NUnit exp-project.Tests.dll'
          }
        }

      }
    }

  }
}