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

    stage('Build') {
      steps {
        sh 'run scripts/build.sh'
      }
    }

  }
  environment {
    registry = 'dbarkov/ci-cd-pipeline-task'
  }
}