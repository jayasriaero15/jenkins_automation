pipeline {
    agent any
    stages {
        stage('Test GitHub OIDC Clone') {
            steps {
                withCredentials([string(credentialsId: 'github-oidc-2', variable: 'ID_TOKEN')]) {
                    bat '''
                        echo Authenticating with GitHub using OIDC...
                        python 
                    '''
                }
            }
        }
    }
}
