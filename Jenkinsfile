pipeline {
  agent any
  stages {
    stage('SCM') {
      steps {
        git 'https://github.com/mpociot/whiteboard.git'
        sh 'ls'
      }
    }
    stage('SonarQube analysis') {
         steps {
             script {
                 withSonarQubeEnv('SonarQubeServerBPittens') {
                
                def scannerHome = tool 'sonarScanner';
                //sonar.projectKey="tnextest1"
                sh "${scannerHome}/bin/sonar-scanner"
                }
            }      
        }
     }    
  }
}
