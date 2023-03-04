pipeline {
  agent any
  
  stages {
    stage('Example') {
      steps {
        sh 'echo "Hello, world!"'
        sh 'ls -lart'
        sh 'docker build -t myimage .'
        sh 'docker run -p 8080:80 myimage'
      }
    }
  }
}
