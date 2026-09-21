pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        checkout([$class: 'GitSCM',
          branches: [[name: '*/main']],
          userRemoteConfigs: [[
            url: 'https://github.com/jayasriaero15/jenkins_automation.git',
            credentialsId: 'github-app-jenkins'
          ]],
          gitTool: 'DefaultGit'
        ])
      }
    }
  }
}
