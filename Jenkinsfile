pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ hello.cpp -o hello_exec'  // Modify if inside a subfolder
            }
        }
        stage('Test') {
            steps {
                sh './hello_exec'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment successful!'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}

