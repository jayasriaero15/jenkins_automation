pipeline {
    agent any
    stages {
        stage('Test GitHub OIDC Clone') {
            steps {
                withCredentials([string(credentialsId: 'github-oidc-2', variable: 'ID_TOKEN')]) {
                    bat '''
                        echo Authenticating with GitHub using OIDC...
                        git config --global http.extraHeader "Authorization: Bearer %ID_TOKEN%"
                        git clone https://github.com/jayasriaero15/jenkins_automation.git
                        dir jenkins_automation
                    '''
                }
            }
        }
    }
}
