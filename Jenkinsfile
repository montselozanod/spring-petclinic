pipeline {
  agent any
  stages {
    stage('Build Application') {
      steps {
        sh '''./mvnw package
'''
      }
    }

    stage('Copy PetClinic Jar') {
      parallel {
        stage('Copy PetClinic Jar') {
          steps {
            sh 'sudo docker cp jenkins-blueocean:/var/jenkins_home/workspace/spring-petclinic_main/target/spring-petclinic-2.7.0-SNAPSHOT.jar /home/malozanod/devOps-assignment1/petclinic.jar'
          }
        }

        stage('Execute Application') {
          steps {
            sh 'java -Dserver.port=8888 -jar target/*.jar'
          }
        }

      }
    }

  }
}