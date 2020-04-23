pipeline {
  stages { 
    stage('Clone') {
      steps {
        git 'https://github.com/jenkinsci/git-plugin'
      }
    }
    stage('Build') {
      steps {
        cd git-plugin
        mkdir -p build
        cmake ..
        cmake --build .
      }
    }
  }
}