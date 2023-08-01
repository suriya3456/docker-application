pipeline {
    agent any
    stages {

        stage('Clone Repo') {
          steps {
            sh 'rm -rf dockertest1'
            sh 'git clone https://github.com/jayasurya9666/dockertest1.git'
            }
        }

        stage('Build Docker Image') {
          steps {
            sh 'docker build -t jayasurya/webapp1:${BUILD_NUMBER} .'
            }
        }

        stage('Push Image to Docker Hub') {
          steps {
           sh    'docker push jayasurya/webapp1:${BUILD_NUMBER}'
           }
        }

stage('Deploy to Docker Host') {
          steps {
            sh    'docker -H tcp://10.0.1.40:2375 stop webapp1 || true'
            sh    'docker -H tcp://10.0.1.40:2375 run --rm -dit --name webapp1  -p 8000:80 jayasurya/webapp1:${BUILD_NUMBER}'
            }
        }

    }
}
