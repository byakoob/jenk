pipeline {
  agent {
    node {
      label 'master'
    }

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

    stage('Buzz Step') {
      steps {
        sh 'echo "I\'m a buzz step!!!"'
        archiveArtifacts(artifacts: '*', fingerprint: true)
      }
    }

  }
}