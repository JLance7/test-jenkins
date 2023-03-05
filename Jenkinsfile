pipeline {
  agent any
  stages {
    stage('build'){
      steps{
        echo 'hi'
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
      }
    }
  }
}