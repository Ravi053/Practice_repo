pipeline {
  agent none;
  stages {
    stage('Build') {
      agent {label 'master'}
      steps {
        echo "this is stage1"
        sh '''
        sleep 3
        '''
      }
    }
    stage('test') {
      parallel {
        stage('slave1') {
          agent {label 'label1'}
          steps {
            echo "this is slave1"
            sh '''
            sleep 3
            '''
          }
        }
        stage('slave2') {
          agent {label 'label1'}
          steps {
            echo "this is slave2"
            sh '''
            sleep 3
            '''
          }
        }
      }
    }
    stage {
      stage('Deploy') {
        agent any;
        steps {
          echo "this is deploy stage"
          sh '''
          sleep 3
          '''
        }
      }
    }
  }
}

    
  
