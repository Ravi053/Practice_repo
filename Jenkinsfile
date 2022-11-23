pipeline {
  agent any;
  stages {
    stage('build') {
      steps {
        echo "this is build stage"
        sh '''
        sleep 3
        '''
      }
    }
    stage('test parallel') {
    parallel {
      stage('product1') {
        steps {
          echo "this is product1"
          sh '''
          sleep 3
          '''
        }
      }
      stage('product2') {
        steps {
          echo "this is product2"
          sh '''
          sleep 3
          '''
        }
      }
    }
  }
  stage('production') {
    steps {
      echo "this is production stage"
    }
  }
}
}


