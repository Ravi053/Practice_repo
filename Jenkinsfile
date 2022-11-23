pipeline {
  agent any;
  stages {
    stage('build') {
      steps {
        echo "this is to test buid timezone"
        sh '''
        systemctldate
        '''
      }
    }
    
