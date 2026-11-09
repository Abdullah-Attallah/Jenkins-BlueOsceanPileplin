pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Building Application'
            }
        }

        stage('Test') {
            steps {
                echo 'Running Tests'
                sh 'python3 app.py'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy Stage'
            }
        }
    }

    post {

        success {
            echo 'Build Succeeded'
        }

        failure {
            echo 'Build Failed'
        }

        always {
            cleanWs()
        }
    }
}
