pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        script {
          checkout scm
          def customImage = docker.build("${registry}:latest")
        }

      }
    }

  }
  environment {
    registry = 'dbarkov/ci-cd-pipeline-task'
  }
}