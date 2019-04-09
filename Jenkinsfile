pipeline {
  agent any
  stages {
    stage('Lint & Unit Test') {
      parallel {
        stage('Lint & Unit Test') {
          steps {
            sh 'chmod +x gradlew'
            sh './gradlew clean'
            sh './gradlew assembleDebug'
          }
        }
        stage('Unit Test') {
          steps {
            sh './gradlew test'
          }
        }
        stage('Lint Test') {
          steps {
            sh './gradlew lint'
          }
        }
      }
    }
    stage('UI test') {
      steps {
        sh 'echo "Use Test suite here"'
      }
    }
    stage('Deploy') {
      steps {
        sh 'echo "Deploy stage"'
      }
    }
  }
}