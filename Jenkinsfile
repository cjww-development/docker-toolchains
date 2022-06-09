pipeline {
  agent {
    docker {
      image 'docker:latest'
      args '--dns 172.17.0.2'
    }
  }
  options {
    ansiColor('xterm')
  }
  stages {
    stage('Build Scala toolchain') {
      environment {
        DOCKER_HOST = credentials('docker-tcp-host')    
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
