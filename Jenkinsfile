pipeline {
  agent any;
  parameters {
  choice choices: ['QA'], description: 'deploying to Branch', name: 'Branch'
    string defaultValue: 'UAT', description: 'deploy to UAT', name: 'ENV', trim: true
}
  environment {
    DEPLOY_BRANCH = "$Branch"
    DEPLOY_ENV = "$ENV"
  }
  stage('build') {
    steps {
      echo "deploying to ${params.Branch}"
      echo "deploying to ${params.ENV}"
      sh '''
      sleep 5
      '''
    }
  }
}
