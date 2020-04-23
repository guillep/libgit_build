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
        sh 'mkdir -p git-plugin/build'
        dir('git-plugin/build') {
          sh 'cmake ..'
          sh 'cmake --build .'
        }        
      }
    }
  }
}