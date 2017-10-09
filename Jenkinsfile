pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        bat(script: 'echo Build', returnStdout: true)
      }
    }
    stage('Browser Tests') {
      steps {
        parallel(
          "Firefox": {
            bat 'echo Browser Test'
            bat 'echo Firefox'
            
          },
          "Safari": {
            bat 'echo Safari'
            
          },
          "Chrome": {
            bat 'echo Chrome'
            
          },
          "Internet Explorer": {
            bat 'echo IE'
            
          }
        )
      }
    }
    stage('Static Analysis') {
      steps {
        bat 'echo Static Analysis'
      }
    }
    stage('Deploy') {
      steps {
        bat 'echo Deploy'
      }
    }
  }
}