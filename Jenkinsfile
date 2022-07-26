pipeline {
  agent any
  stages {
    stage('Build Application') {
      steps {
        sh '''./mvnw package
java -jar target/*.jar'''
      }
    }

  }
}