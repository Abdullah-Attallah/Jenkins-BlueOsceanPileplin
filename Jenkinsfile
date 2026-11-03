pipeline {
    agent any

 

        stage('Run App') {
            steps {
                sh 'python3 app.py'
            }
        }
    }

    post {
        success { echo 'Build succeeded' }
        failure { echo 'Build failed' }
        always  { cleanWs() }
    }
}
