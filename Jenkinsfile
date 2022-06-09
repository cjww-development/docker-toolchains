pipeline {
  agent {
    docker {
      image 'docker:latest'
      args '--network="host"'
    }
  }
  options {
    ansiColor('xterm')
  }
  stages {
    stage('Build Scala toolchain') {
      environment {
        DOCKER_HOST = 'tcp://127.0.0.1:2375'
      }
      steps {
        sh "docker build -t cjww-development/scala-toolchain:latest -f scala-toolchain/Dockerfile ."
      }
    }
  }
  post {
    always {
      cleanWs()
    }
  }
}
