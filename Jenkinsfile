pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        script {
          checkout scm
        }

      }
    }

  }
  environment {
    registry = 'dbarkov/ci-cd-pipeline-task'
  }
}