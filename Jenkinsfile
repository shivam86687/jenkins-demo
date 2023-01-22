pipeline {
  agent any
  stages {
    stage('Test') {
      steps {
        echo 'testing done'
      }
    }

    stage('Snapshot build') {
      parallel {
        stage('Snapshot build') {
          steps {
            echo 'building snapshot'
          }
        }

        stage('working dir') {
          steps {
            sh 'pwd'
          }
        }

      }
    }

    stage('Release build') {
      parallel {
        stage('Release build') {
          steps {
            echo 'building release'
          }
        }

        stage('acceptance testing') {
          steps {
            sh 'sleep 10'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        sh 'date'
        echo 'deploying'
      }
    }

  }
}