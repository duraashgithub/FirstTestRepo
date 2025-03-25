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
          steps {
            sh 'echo this is parallel stage'
          }
        }

      }
    }

    stage('Fluffy Test') {
      steps {
        sh 'sleep 5'
        sh 'echo success!'
      }
    }

  }
}