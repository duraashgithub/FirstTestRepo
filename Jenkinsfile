pipeline {
  agent none
  stages {
    stage('Buzz') {
      parallel {
        stage('Buzz') {
          agent {
            label 'BuiltIn'
          }
          steps {
            echo 'Bees Buzz'
          }
        }

        stage('Parallel stage') {
          agent {
            label 'BuiltIn'
          }
          steps {
            sh 'echo this is parallel stage'
            stash(name: 'TestStash', includes: '*.*')
          }
        }

      }
    }

    stage('Fluffy Test') {
      agent {
        label 'BuiltIn'
      }
      steps {
        sh 'echo success!'
        unstash 'TestStash'
      }
    }

    stage('Confirm') {
      steps {
        input(message: 'Deploy to stage', ok: 'Yes')
      }
    }

    stage('deploy to stage') {
      steps {
        echo 'deployment sucess'
      }
    }

  }
}