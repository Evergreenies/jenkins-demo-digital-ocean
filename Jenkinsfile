pipeline {
  agent any
  stages {
    stage('build') {
      parallel {
        stage('build') {
          steps {
            sh '''echo "building"
sleep 10'''
          }
        }

        stage('linting') {
          steps {
            sh '''echo "linting"
sleep 10'''
          }
        }

      }
    }

    stage('test') {
      steps {
        sh '''echo "testing"
sleep 10'''
      }
    }

    stage('deploy-dev') {
      steps {
        sh '''echo "deploying to dev"
sleep 10'''
      }
    }

    stage('deploy-stage') {
      steps {
        sh '''echo "deploy to stage"
sleep 10'''
      }
    }

    stage('deploy-prod') {
      steps {
        sh '''echo "deploy to prod"
sleep 10'''
        input(message: 'Would you like to continue?', id: 'deploy-to-prod', ok: 'Yes please')
      }
    }

  }
}