pipeline {
  agent any
  stages {
    stage('Build Application') {
      steps {
        sh '''./mvnw package -Dserver.port=8888
java -Dserver.port=8888 -jar target/*.jar'''
      }
    }

  }
}