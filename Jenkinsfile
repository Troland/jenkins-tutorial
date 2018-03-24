pipeline {
  agent any
  parameters {
    string(name: 'Greeting', defaultValue: 'Hello', description: 'How should I greet the world?')
  }
  stages {
    stage('Build') {
      steps {
        echo "${params.Greeting} World!"
      }
    }
    stage('Test') {
      steps {
        echo "test"
      }
    }
    stage('Deploy') {
      when {
        expression {
          currentBuild.result == null || currentBuild.result == 'SUCCESS'
        }
      }
      steps {
        echo 'finished'
      }
    }
  }
  post {
    always {
      sh 'ls'
    }
  }
}
