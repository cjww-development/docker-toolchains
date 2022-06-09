pipeline {
  agent {
    docker {
      image 'docker:latest'
      args '-v /var/run/docker.sock:/var/run/docker.sock -u jenkins:jenkins'
    }
  }
  options {
    ansiColor('xterm')
  }
  stages {
    stage('Build Scala toolchain') {
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
