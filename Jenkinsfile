pipeline {
    agent any
    
    stages {
        stage('Clone Repository') {
            steps {
                script {
                    sh 'rm -rf PES1UG22CS34_Jenkins' // Remove existing directory
                    sh 'git clone https://github.com/meghnaroyal/PES1UG22CS34_Jenkins.git'
                }
            }
        }

        
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o PES1UG22CS334-1 PES1UG22CS34_Jenkins/working.cpp'
                }
            }
        }
        
        stage('Test') {
            steps {
                script {
                    sh './PES1UG22CS334-1'
                }
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'deploy'
                // Add deployment steps here
            }
        }
    }
    stage('Verify Files') {
        steps {
            sh 'ls -R'
        }
    }

    
    post {
        failure {
            echo 'pipeline failed'
        }
    }
}
