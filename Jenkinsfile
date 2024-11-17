pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'build competed '
        retry(count: 3) {
          echo 'try to build'
        }

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
        input(message: 'Are you to deploy ?', ok: 'Yes I am sure ')
        echo 'Deployment completed '
      }
    }

    stage('Notify for new build') {
      steps {
        echo 'new build completed successful'
      }
    }

  }
}