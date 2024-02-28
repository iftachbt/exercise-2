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
            sh 'docker build -t db ./db'
          }
        }

        stage('flask') {
          steps {
            sh 'docker build -t flask ./flask'
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