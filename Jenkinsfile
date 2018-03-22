pipeline {
  agent { docker { image 'node:7-alpine' } }
  stages {
    stage('build') {
      steps {
        sh 'node --version'
      }
    }
  }

  post {
    always {
      mail to: 'new-band007@163.com',
           subject: "Build Failed: ${currentBuild.fullDisplayName}",
           body: "Something is wrong ${env.BUILD_URL}"
    }
  }
}
