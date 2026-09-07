pipeline {
    agent any
    stages {
        stage('Run Python with GitHub OIDC') {
            steps {
                withCredentials([string(credentialsId: 'github-oidc-2', variable: 'ID_TOKEN')]) {
                    bat '''
                        git config --global http.extraHeader "Authorization: Bearer %ID_TOKEN%"
                        git clone https://github.com/jayasriaero15/jenkins_automation.git
                        python python_print.py
                    '''
                }
            }
        }
    }
}
