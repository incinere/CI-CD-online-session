pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        script {
          checkout scm
          def customImage = docker.build("${registry}:${env.Build_ID}")
        }

      }
    }

  }
  environment {
    registry = 'docker push incinere/flask-app'
  }
}