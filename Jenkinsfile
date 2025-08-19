pipeline {
    agent { label 'AGENT-1' }
    environment {
        PROJECT = 'EXPENSE'
        COMPONENT = 'BACKEND'
    }
    options {
        disableConcurrentBuilds()
    }
    stages {
        stage('Build') {
            steps {
                script{
                    sh """
                    echo "Hello, This is Build"
                    echo "Project: $PROJECT"
                    """
                }
            }
        }
        stage('Test') {
            steps {
                script{
                    sh """
                    echo "Hello, This is Test"
                    """
                }
            }
        }
        stage('Deploy') {
            steps {
                script{
                    sh """
                    echo "Hello, This is Deploy"
                    """
                }
            }
        }
    }
    post {
        always {
            echo 'I will always say Hello again!'
        }
        failure {
            echo 'I will run when pipeline is failed'
        }
        success {
            echo 'I will run when pipeline is success'
        }
    }
}