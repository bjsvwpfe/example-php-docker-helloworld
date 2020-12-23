pipeline {
  agent any
  stages {
    stage('prod') {
      steps {
        library 'jenkins-shared-libs'
      }
    }
    stage('int') {
      steps {
        build 'test'
      }
    }
    stage('test') {
      parallel {
        stage('test') {
          steps {
            sleep 5
          }
        }
        stage('') {
          steps {
            sleep 10
          }
        }
      }
    }
  }
}