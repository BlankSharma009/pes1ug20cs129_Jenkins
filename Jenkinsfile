pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        sh 'g++ -o cs129 cs129.cpp'
        build job: 'pes1ug20cs129-1'
        echo "BUILD successful"
      }
    }
    stage('Test') {
      steps {
        sh './cs129'
        echo "TEST successful"
      }
    }
    stage('Deploy') {
      steps {
        sh 'echo "Deployment stage"'
        sh 'exit 1'
        echo "DEPLOY successful"
      }
    }
  }

  post {
    failure {
     echo 'Pipeline failed.'
    }
  }
}
