pipeline {
  agent none
  stages {
    stage('testbuild') {
      steps {
        echo 'test build'
      }
    }

    stage('test done') {
      steps {
        echo 'test done'
      }
    }

    stage('test python version') {
      steps {
        bat 'python --version'
      }
    }
  }
}
