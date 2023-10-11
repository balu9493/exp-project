pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        script {
                    // Use the correct SCM checkout step based on your SCM (Git in this case)
                    git(url: 'https://github.com/balu9493/exp-project', branch: 'main')
          }
      }
    }

    stage('') {
      steps {
        script {
                    // Use 'bat' on Windows and 'sh' on Unix-like systems
                    if (isUnix()) {
                        sh 'ls -la'
                    } else {
                        bat 'dir'
                    }
        }
      }
    }

  }
}