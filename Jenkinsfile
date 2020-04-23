pipeline {
  agent { label 'osx' }
  stages { 
    stage('Clone') {
      steps {
        sh 'git clone https://github.com/libgit2/libgit2.git libgit2'
      }
    }
    stage('Build') {
      steps {
        sh 'mkdir -p libgit2/build'
        dir('libgit2/build') {
          sh 'cmake ..'
          sh 'cmake --build .'
        }        
      }
    }
  }
}