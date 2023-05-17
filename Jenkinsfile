pipeline {
  agent any
  stages {
    stage('build') {
      steps {
       sh 'pip install -r requirements.txt'
      }
    }
    stage('test') {
      steps {
        sh 'puthon test.py'
      }
      post {
        always{
          junit 'test-reports/*.xml'
        }
      }
    }
  }
}
