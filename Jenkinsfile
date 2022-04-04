pipeline {
  
  options {
        office365ConnectorWebhooks([
            [name: "Office 365", url: "https://infogain.webhook.office.com/webhookb2/403b46f3-db2f-4192-826d-b7634c9d14c6@3f7f52c7-07b2-4cb1-a07a-496256021e6f/JenkinsCI/5289d11afdf4438b892c4d05bb470c0d/480784c9-926b-412d-8eef-d7407e356dc6", notifyBackToNormal: true, notifyFailure: true, notifyRepeatedFailure: true, notifySuccess: true, notifyAborted: true]
        ])
    }
  agent any
  stages {
    stage('build') {
      steps {
        bat 'mvn clean'
      }
    }

    stage('test') {
      steps {
        bat 'mvn test'
      }
    }

    stage('deploy') {
      steps {
        bat 'mvn package'
      }
    }

  }
}
