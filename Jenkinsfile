pipeline {
  agent any
  stages {
    stage('clone') {
      steps {
        git 'https://github.com/Andrew-1995/spring-boot-mongo-docker-.git'
      }
    }

    stage('Build Image') {
      steps {
        sh 'docker build -t 3226555/angular:2020 .'
      }
    }

  }
}