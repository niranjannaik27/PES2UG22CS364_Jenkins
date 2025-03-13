pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g++-wrong -o PES2UG22CS364-1 PES2UG22CS364-1.cpp'
                echo 'Build Stage Successful'
            }
        }
        
        stage('Test') {
            steps {
                sh './PES2UG22CS364-1'
                echo 'Test Stage Successful'
            }
        }
        
        stage('Deploy') {
            steps {
                sh 'echo Deploying the application'
                echo 'Deployment Successful'
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
