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
                // Execute Batch script commands
                script {
                    bat 'nuget restore exp-project.sln'
                    bat 'msbuild exp-project.sln'
                    bat 'nunit-console exp-project.Tests.dll'
                }
            }
        }


      }
    }

  }
}
