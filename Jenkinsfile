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

      stage('Unit Tests') {
            steps {
                // Execute Batch script commands
                script {
                    bat '''
                        @echo off
                        echo Installing Node.js dependencies
                        npm install

                        echo Running unit tests
                        npm test
                    '''
                }
            }
        }


      }
    }

  }
}
