pipeline {
    agent any
    stages {
        stage('Git Checkout'){
            steps {
                git 'https://github.com/formycore/nodejs_vamsi.git'
            }
        }
        stage ('Node Build') {
            steps {
                nodejs(nodeJSInstallationName: 'nodejs18') {
                    sh "npm install"
                }
            }
        }
        stage ('Node sonar scan') {
            steps {
                nodejs(nodeJSInstallationName: 'nodejs18') {
                    sh "npm run sonar"
                }
            }
        }

    }
}
