pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        
        stage('Linting') {
            when {
                expression { env.BRANCH_NAME == 'main' }
            }
            
            steps {
                sh 'pip install --upgrade flake8'
                sh 'flake8 --exclude=venv'
            }
        }
        
        stage('Build') {
            when {
                branch 'master'
            }
            
            
        }
        
        stage('Test') {
            when {
                branch 'master'
            }
            
         
        }
        
        stage('Deploy') {
            when {
                branch 'master'
            }
            
            
        }
    }
}
