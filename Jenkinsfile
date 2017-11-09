pipeline {
  agent any
  stages {
    stage('Stage 1') {
      environment {
        var = '1'
      }
      steps {
        sh 'echo "Hello Blue Ocean from state 1"'
      }
    }
    stage('Stage 2') {
      steps {
        echo 'Now in stage 2'
        waitUntil() {
          sh '''echo "Finish waiting at step 2"
echo $var'''
        }
        
      }
    }
  }
  environment {
    var = '0'
  }
}