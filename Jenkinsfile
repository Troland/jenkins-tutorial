pipeline {
  agent any
  stages {
    stage('myStage'){
      steps {
        echo 'branch test sage'
      }
    }
    stage('Build') {
      steps {
        echo "branch-${BRANCH_NAME} test build"
      }
    }
  }
}
