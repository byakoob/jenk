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
      steps {
        sh 'echo \'Testing..\''
      }
    }

  }
}