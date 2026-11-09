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

        stage('Security Check') {
            steps {
                echo 'Security Scan Started'
            }
        }

        stage('Package') {
            steps {
                echo 'Packaging Application'
                sh 'tar -czf app.tar.gz app.py'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying Application'
            }
        }
    }

    post {

        success {
            echo 'Pipeline Succeeded'
        }

        failure {
            echo 'Pipeline Failed'
        }

        always {
            cleanWs()
        }
    }
}
