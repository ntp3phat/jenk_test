pipeline {
  agent any
  stages {
    stage('checkout Code') {
      parallel {
        stage('checkout Code') {
          steps {
            git(url: 'https://github.com/ntp3phat/jenk_test', branch: 'main')
          }
        }

        stage('list file') {
          steps {
            sh 'ls -lt'
          }
        }

      }
    }

    stage('list data') {
      steps {
        sh 'ls -lh'
      }
    }

    stage('run unit test') {
      steps {
        sh 'cd curriculum-front && npm install'
      }
    }

    stage('build image') {
      steps {
        sh 'docker build -f curriculum-front/Dockerfile .'
      }
    }

  }
}