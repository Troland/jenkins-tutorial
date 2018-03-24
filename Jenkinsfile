pipeline {
  agent any
  parameters {
    string(name: 'Greeting', defaultValue: 'Hello')
  }
  stages {
    stage('Build') {
      steps {
        echo "${params.Greeting} World!"
      }
    }
    stage('Test') {
      steps {
        echo "$"
      }
    }
    stage('Deploy') {
      when {
        expression {
          currentBuild.result == null || currentBuild.result == 'SUCCESS'
        }
      }
      steps {
        sh 'make publish'
      }
    }
  }
  post {
    always {
      sh 'ls'
    }
  }
}
