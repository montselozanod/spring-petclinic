pipeline {
  agent any
  stages {
    stage('error') {
      steps {
        sh '''sh \'./mvnw package\'
sh \'java -jar target/*.jar\''''
      }
    }

  }
}