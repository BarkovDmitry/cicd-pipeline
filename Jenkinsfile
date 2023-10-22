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
          sh('chmod +x build.sh')
          sh('./build.sh')
        }
      }
    }

    stage('Tests') {
      steps {
        dir ('scripts') {
          sh('./test.sh')
        }
      }
    }
    
    stage('Build image') {
      steps {
        script {
          docker.build("${registry}:latest")
        }

      }
    }

  }
  environment {
    registry = 'dbarkov/ci-cd-pipeline-task'
  }
}
