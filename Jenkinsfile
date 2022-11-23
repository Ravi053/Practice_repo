pipeline {
  agent any;
  parameters {
  string defaultValue: 'test', description: 'deploying to ENV', name: 'ENV', trim: true
     choice choices: ['test'], description: 'deploying to Branch', name: 'Branch'
}
  environment {
    DEPLOY_BRANCH = "$Branch"
    DEPLOY_ENV = "$ENV"
  }
  stages {
    stage('Build') {
      steps {
        echo "deploying to ${params.Branch}"
        echo "deploying to ${params.ENV}"
        sh '''
        sleep 3
        '''
      }
    }
    stage('parallel') {
      parallel {
        stage('slave1') {
          agent {label 'label1'}
          steps {
            echo "$NAME"
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


    
  
