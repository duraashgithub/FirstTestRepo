pipeline {
  agent any
  environment {
    globalenv = " GlobalEnv Test"
  }
  stages {
    stage('Buzz') {
      parallel {
        stage('Buzz') {
            environment {
                 Buzzenv = "  buzz Env Test"
               }
          steps {
            echo 'Bees Buzz'
            sh 'printenv'
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
