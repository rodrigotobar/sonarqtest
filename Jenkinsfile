pipeline {
  agent any
  stages {
    stage('SCM') {
      steps {
        git 'https://github.com/mpociot/whiteboard.git'
        sh 'ls'
      }
    }
  }
}