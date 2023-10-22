node {
    checkout scm

    docker.image('node:16-buster-slim').inside('-p 4000:4000') {
        stage('Build') {
            sh 'npm install'
        }
        stage('Test') {
            sh './jenkins/scripts/test.sh'
        }
    }
}