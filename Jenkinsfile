pipeline {
  agent any
  stages {
    stage('Build Application') {
      steps {
        sh '''./mvnw package
'''
      }
    }

   stage('Deployment') {
      steps {
        sh "whoami"
        ansiblePlaybook(disableHostKeyChecking: true, installation: 'ansible', inventory: 'dev.inv', playbook: 'playbook.yml')
      }
    }
  }
}
