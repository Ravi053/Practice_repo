pipeline {
  agent any;
  parameters {
  string defaultValue: 'SIT', description: 'deploying to ENV', name: 'ENV', trim: true
     choice choices: ['QA'], description: 'deploying to Branch', name: 'Branch'
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
  }
}
