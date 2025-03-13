pipeline {
    agent any
    
    stages {
        stage('Clone Repository') {
            steps {
                sh 'rm -rf PES1UG22CS34_Jenkins'
                sh 'git clone https://github.com/meghnaroyal/PES1UG22CS34_Jenkins.git'
            }
        }

        stage('Verify Files') {
            steps {
                sh 'ls -R'
            }
        }

        stage('Build') {
            steps {
                sh 'g++ -o PES1UG22CS334-1 PES1UG22CS34_Jenkins/working.cpp'
            }
        }
    }

    post {
        failure {
            echo 'pipeline failed'
        }
    }
}
