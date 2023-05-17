pipeline {
    agent any

    environment {
        // Application settings
        APP_NAME = "jenkins-playground"
        TRUNK_BRANCH = "master"
        PIPELINE_URL = "${env.RUN_DISPLAY_URL != null ? env.RUN_DISPLAY_URL : env.RUN_CHANGES_DISPLAY_URL}"

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
