pipeline{
    agent any
    stages {
        // This should run for every commit of feature branch
        stage('Lint checks') {
            steps {
                sh "echo installing jslint"
                sh "npm install jslint"
                sh "ls -ltr node_modules/jslint/bin"
                sh "~/node_modules/jslint/bin/jslint.js server.js"
            }
        }
    }
}