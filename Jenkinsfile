pipeline {
  agent any
  stages {
    stage('Stage1') {
      parallel {
        stage('Stage1') {
          steps {
            echo 'Hello $BUILD_NUMBER'
            sh 'echo "this is ${BUILD_NUMBER}"'
          }
        }

        stage('Stage1.1') {
          steps {
            sh 'echo "this is stage1.1"'
          }
        }

      }
    }

    stage('stage2') {
      steps {
        sh 'echo "environment: ${env}"'
      }
    }


  }
  environment {
    env = 'bts'
  }
}