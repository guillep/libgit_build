pipeline {
  agent any
  stages { 
    stage('Clone') {
      steps {
        sh 'git clone https://github.com/jenkinsci/git-plugin'
      }
    }
    stage('Build') {
      steps {
        cd git-plugin
        sh 'mkdir -p build'
        sh 'cmake ..'
        sh 'cmake --build .'
      }
    }
  }
}