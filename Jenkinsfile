pipeline {
    agent any
    stages {

        stage('Clone Repo') {
          steps {
            sh 'rm -rf dockertest1'
            sh 'git clone git@github.com:jayasurya9666/dockertest1.git'
            }
        }

        stage('Build Docker Image') {
          steps {
            sh 'docker build -t jayasurya/sampledocker:${BUILD_NUMBER} .'
            }
        }

        stage('Push Image to Docker Hub') {
          steps {
           sh    'docker push jayasurya/sampledocker:${BUILD_NUMBER}'
           }
        }
