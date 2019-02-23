pipeline {
  agent any
  stages {
    stage('SCM') {
      steps {
        script {
        git 'https://github.com/mpociot/whiteboard.git'
        sh 'ls'
        sh 'pwd'
        }
      }
    }
    stage('SonarQube analysis') {
         steps {
             script {
                 withSonarQubeEnv('jenkins') {
                 def scannerHome = tool 'sonarScanner';
                //sonar.projectKey="tnextest1"
                sh "${scannerHome}/bin/sonar-scanner"
                }
            }      
        }
     }    
  }
}
