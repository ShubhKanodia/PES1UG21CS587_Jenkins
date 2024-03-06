pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building...'

                build 'PES1UG21CS587-1'

                sh 'g++ main.cpp -o output'
            }
        }
        
        stage('Test') {
            steps {
                echo 'Testing...'
               
                sh './output'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploy'
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
