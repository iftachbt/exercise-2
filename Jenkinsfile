pipeline {
  agent any
  stages {
    stage('build') {
      parallel {
        stage('proxy') {
          steps {
            sh 'docker build -t proxy ./proxy'
          }
        }

        stage('db') {
          steps {
            sh 'sh \'echo \\\'db...\\\'\''
          }
        }

        stage('flask') {
          steps {
            sh 'docker build -t backend ./backend'
          }
        }

      }
    }

    stage('test') {
      steps {
        sh 'docker images'
      }
    }

  }
}