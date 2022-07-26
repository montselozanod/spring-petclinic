pipeline {
  agent any
  stages {
    stage('Build Application') {
      steps {
        sh '''./mvnw package
java -Dserver.port=8888 -jar target/*.jar'''
      }
    }

  }
}