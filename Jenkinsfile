pipeline {
  agent any
  stages {
    stage('clone') {
      parallel {
        stage('clone') {
          steps {
            git 'https://github.com/Andrew-1995/spring-boot-mongo-docker-.git'
          }
        }

        stage('Clean Pkg') {
          steps {
            sh '''        def mvnHOME = tool name: \'maven-3\', type: \'maven\'
        def mvnCMD = "${mvnHOME}/bin/mvn"
        sh "${mvnCMD} clean package"'''
          }
        }

      }
    }

    stage('Build Image') {
      steps {
        sh 'docker build -t 3226555/angular:2020 .'
      }
    }

  }
}