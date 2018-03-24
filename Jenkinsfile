pipeline {
  agent {
    docker { image 'node:7-alpine' }
  }
  stages {
    stage('myStage'){
      steps {
        sh 'node --version'
      }
    }
    stage('Build') {
      steps {
        echo "branch-${BRANCH_NAME} test build"
      }
    }
  }
}
