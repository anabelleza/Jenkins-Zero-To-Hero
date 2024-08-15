# A simple jenkins pipeline to verify if the docker slave configuration is working as expected.
# Original Jenkinsfile of this project
pipeline {
  agent {
    docker { image 'node:16-alpine' }
  }
  stages {
    stage('Test') {
      steps {
        sh 'node --version'
        ls -al
      }
    }
  }
}
