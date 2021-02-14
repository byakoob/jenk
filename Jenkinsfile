pipeline {
  agent {
    label 'master'
  }
  stages {
    stage('build') {
      steps {
        sh 'uname -a'
      }
    }

    stage('test') {
      agent {
        node {
          label 'master'
        }

      }
      steps {
        sh 'echo "I\'am a test"'
      }
    }

  }
}