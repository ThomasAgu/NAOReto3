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
                expression { env.BRANCH_NAME == 'master' }
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
            
            steps {
                
                // Agrega aquí tus pasos de construcción
            }
        }
        
        stage('Test') {
            when {
                branch 'master'
            }
            
            steps {
                // Agrega aquí tus pasos de prueba
            }
        }
        
        stage('Deploy') {
            when {
                branch 'master'
            }
            
            steps {
                // Agrega aquí tus pasos de despliegue
            }
        }
    }
}
