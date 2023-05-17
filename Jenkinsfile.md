pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building..'
      }
    }

    stage('Test') {
      steps {
        echo 'Testing..'
      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying....'
      }
    }

  }
  environment {
    APP_NAME = 'jenkins-playground'
    TRUNK_BRANCH = 'master'
  }
  options {
    timeout(time: 45, unit: 'MINUTES')
  }
}