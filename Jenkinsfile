@Library('roboshop-shared-library@main')
pipeline{
    agent any
    stages {
        // This should run for every commit of feature branch
        stage('Lint checks') {
            steps {
                script {
                    sample.info("Starting-value", "snapchat.com")
                }
                sh "echo installing jslint"
                sh "npm install jslint"
                sh "ls -ltr node_modules/jslint/bin"
                sh "~/node_modules/jslint/bin/jslint.js server.js || true"
                sh "echo lint checks completed"

            }
        }
    }
}