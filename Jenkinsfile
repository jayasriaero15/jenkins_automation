pipeline {
    agent any
    stages {
        stage('Run Python') {
            steps {
                // Use OIDC token for GitHub authentication
                withCredentials([string(credentialsId: 'github-oidc-2', variable: 'ID_TOKEN')]) {
                    sh '''
                        git config --global http.extraHeader "Authorization: Bearer $ID_TOKEN"
                        git clone https://github.com/jayasriaero15/jenkins_automation.git
                        python python_print.py
                    '''
                }
            }
        }
    }
}
