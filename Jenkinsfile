pipeline {
    agent any

    stages {

        stage('Show Secret') {
            steps {
                withCredentials([
                    string(
                        credentialsId: 'demo-secret',
                        variable: 'MY_SECRET'
                    )
                ]) {

                    sh '''
                        echo "Secret Loaded"
                    '''
                }
            }
        }
    }
}
