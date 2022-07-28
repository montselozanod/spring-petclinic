pipeline {
  agent any
  stages {
    stage('Build Application') {
      steps {
        sh '''./mvnw package
'''
      }
    }

    stage('Sonarqube Analysis') {
      steps {
        withSonarQubeEnv('sonarqube') {
          sh './mvnw clean package sonar:sonar'
        }

      }
    }

    stage('Deployment') {
      steps {
        sh 'java -Dserver.port=8888 -jar target/*.jar'
      }
    }

  }
}