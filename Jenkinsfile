pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'build  started'
      }
    }

    stage('Testing') {
      parallel {
        stage('Testing') {
          steps {
            echo 'testing is in progress'
            bat 'mvn test'
          }
        }

        stage('API testing') {
          steps {
            echo 'API'
          }
        }

        stage('Performance testing') {
          steps {
            echo 'Performance'
          }
        }

      }
    }

  }
}