#!groovy

def app = null;

pipeline {
    agent none
     stages {
        stage('Build') {
            agent { label 'linux-container' }
            steps {
                app = docker.build("platform-sandbox-2028d9/sandbox-demo")
            }
        }
        stage('Push') {
            agent { label 'linux-container' }
            docker.withRegistry('https://us.gcr.io', 'gcr:[platform-sandbox]') {
            }
        }
     }
}