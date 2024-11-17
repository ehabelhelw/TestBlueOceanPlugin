pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'build competed '
      }
    }

    stage('Test Stages') {
      parallel {
        stage('Test 2') {
          steps {
            echo 'Running test2'
          }
        }

        stage('Test1') {
          steps {
            echo 'Running test1'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        echo 'Deployment completed '
      }
    }

  }
}