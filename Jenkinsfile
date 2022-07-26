pipeline {
  agent any
  stages {
    stage('Build Application') {
      steps {
        sh '''./mvnw package
java -Dserver.port=2376 -jar target/*.jar'''
      }
    }

  }
}