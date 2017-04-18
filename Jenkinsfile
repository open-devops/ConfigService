pipeline {
  agent any
  stages {
    stage('Initialize') {
      steps {
        acceptGitLabMR()
      }
    }
    stage('build') {
      steps {
        echo 'deploy'
      }
    }
    stage('test') {
      steps {
        parallel(
          "test": {
            echo 'test'
            
          },
          "junit test": {
            echo 'teset'
            
          },
          "browser test": {
            echo 'test'
            
          }
        )
      }
    }
    stage('deploy') {
      steps {
        echo 'deploy'
      }
    }
  }
}