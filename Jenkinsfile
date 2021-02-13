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
      parallel {
        stage('test') {
          steps {
            sh 'echo \'Testing..\''
          }
        }

        stage('variables') {
          agent {
            node {
              label 'master'
            }

          }
          environment {
            NUM = '603873'
          }
          steps {
            sh 'echo "$NUM"'
          }
        }

        stage('parrallel') {
          steps {
            sh 'kubectl get pods'
          }
        }

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