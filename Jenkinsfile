pipeline {
  agent {
    docker { image 'node:16.13.1-alpine' }
  }
  stages {
    stage('build'){
      steps{
        echo 'hi test 2'
      }
    }
    stage('cat test.txt'){
      when {
        branch "master"
      }
      steps {
        sh '''
          cat test.txt
        '''
        sh 'node --version'
      }
    }
  }
}
