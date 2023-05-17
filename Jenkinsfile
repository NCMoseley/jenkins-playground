pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Custom Build step'
      }
    }

    stage('Sleep') {
      steps {
        sleep 100
      }
    }

    stage('FIN') {
      steps {
        echo 'Finished'
      }
    }

  }
  environment {
    APP_NAME = 'jenkins-playground'
    TRUNK_BRANCH = 'master'
  }
  options {
    timeout(time: 45, unit: 'MINUTES')

    disableConcurrentBuilds(abortPrevious: true)
  }
}