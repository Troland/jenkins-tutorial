pipeline {
  agent { docker { image 'node:7-alpine' } }
  stages {
    stage('Deploy - Staging') {
      steps {
        sh 'node --version'
      }
    }

    stage('Sanity check') {
      steps {
        input "Does the ok?"
      }
    }
  }

  post {
    always {
      sh 'ls'
    }
  }
}
