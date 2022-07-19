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
        sh "docker build -t cjww-development/scala-toolchain:jdk17_2.13.8_1.6.2 -f scala-toolchain/jdk17/scala2.13.8/sbt1.6.2/Dockerfile ."
      }
    }
  }
  post {
    always {
      cleanWs()
    }
  }
}
