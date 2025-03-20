pipeline {
  agent any
  stages {
    stage('Buzz') {
      parallel {
        stage('Buzz') {
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
  environment {
    test = 'val'
  }
}