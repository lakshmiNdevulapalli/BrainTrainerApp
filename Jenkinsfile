pipeline {
  agent any
  stages {
    stage('Lint & Unit Test') {
      parallel {
        stage('Lint & Unit Test') {
          steps {
            sh '''java -version
chmod +x gradlew'''
            sh '''./gradlew clean
chmod 755 /Users/baladevulapalli/Library/Android/sdk'''
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