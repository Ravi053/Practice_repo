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
  }
}
