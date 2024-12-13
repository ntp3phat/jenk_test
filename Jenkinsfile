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

  }
}