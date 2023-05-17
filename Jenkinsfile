pipeline {
    agent any

    environment {
        // Application settings
        APP_NAME = "jenkins-playground"
        TRUNK_BRANCH = "master"
        PIPELINE_URL = "${env.RUN_DISPLAY_URL != null ? env.RUN_DISPLAY_URL : env.RUN_CHANGES_DISPLAY_URL}"

        // GitHub / Pipeline commit Information
        GIT_TAG = "${env.TAG_NAME}"
        CURRENT_BRANCH = "${env.CHANGE_BRANCH != null ? env.CHANGE_BRANCH : env.GIT_BRANCH}"
        GIT_COMMIT_MESSAGE = getLastCommitMessage()
        COMMIT = "${env.GIT_COMMIT[0..7]}"
        WORKSPACE = "${env.WORKSPACE}"
        PARENT_WORKSPACE = "${env.WORKSPACE}"
    }

    // Force the pipeline to timeout and abort after 30min
    options {
        timeout(time: 45, unit: 'MINUTES')
    }

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
}
