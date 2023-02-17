pipeline {
  agent any
  
  stages {
    stage('Build') {
      steps {
        sh 'g++ -o PES2UG20CS031 PES2UG20CS031.cpp'
        echo 'Build stage successful'
      }
    }
    stage('Test') {
      steps {
        sh './PES2UG20CS031'
        echo 'Test stage successful'
      }
    }
    stage('Deploy') {
      steps {
        sh 'echo "Deploying..."'
        echo 'Deployment successful'
      }
    }
  }
  
  post {
    failure {
      echo 'pipeline failed'
    }
  }
}
