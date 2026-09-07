pipeline {
    agent any
    stages {
        stage('Test GitHub OIDC') {
            steps {
                withCredentials([string(credentialsId: 'github-oidc-2', variable: 'ID_TOKEN')]) {
                    bat '''
                        echo Testing GitHub OIDC Authentication...
                        curl -H "Authorization: Bearer %ID_TOKEN%" https://api.github.com/user
                    '''
                }
            }
        }
    }
}
