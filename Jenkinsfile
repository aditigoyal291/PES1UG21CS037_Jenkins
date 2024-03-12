pipeline{
  agent any 
  stages {
    stage('Build') {
      steps {
        build 'PES1UG21CS037_1'
        sh 'cd main \ng++ hello2.cpp -o output'
      }
    }
    stage('Test') {
      steps {
        sh './main/output'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deployed!!'
      }
    }
  }
    post {
      failure {
        error 'Pipeline failed'
      }
    }
}
