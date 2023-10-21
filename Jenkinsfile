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
        dir ('scripts') {
          sh('./build.sh')
        }
      }
    }

  }
  environment {
    registry = 'dbarkov/ci-cd-pipeline-task'
  }
}
