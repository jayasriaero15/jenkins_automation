pipeline {
    agent any
    stages {
        stage('Test GitHub OIDC Clone') {
            steps {
                    bat '''
                        echo Authenticating with GitHub using OIDC...
                        python python_print.py
                    '''
            }
        }
    }
}
