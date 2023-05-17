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
    PIPELINE_URL = "${env.RUN_DISPLAY_URL != null ? env.RUN_DISPLAY_URL : env.RUN_CHANGES_DISPLAY_URL}"
    GIT_TAG = "${env.TAG_NAME}"
    CURRENT_BRANCH = "${env.CHANGE_BRANCH != null ? env.CHANGE_BRANCH : env.GIT_BRANCH}"
    GIT_COMMIT_MESSAGE = getLastCommitMessage()
    COMMIT = "${env.GIT_COMMIT[0..7]}"
    WORKSPACE = "${env.WORKSPACE}"
    PARENT_WORKSPACE = "${env.WORKSPACE}"
  }
  options {
    timeout(time: 45, unit: 'MINUTES')
  }
}