pipeline {
  agent any
  stages {
    stage('checkout Code') {
      steps {
        git(url: 'https://github.com/ntp3phat/jenk_test', branch: 'main')
      }
    }

    stage('list data') {
      steps {
        sh 'ls -lh'
      }
    }

    stage('run unit test') {
      steps {
        sh 'cat curriculum-front/Dockerfile'
      }
    }

    stage('build image') {
      environment {
        user = 'test'
        pass = 'test'
      }
      steps {
        sh 'docker build -f curriculum-front/Dockerfile .'
      }
    }

  }
}