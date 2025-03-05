pipeline {
    agent any
    
    environment {
        NODE_HOME = tool 'NodeJS'
        PATH = "${env.NODE_HOME}/bin:${env.PATH}"
    }
    
    stages {
        stage('Install Dependencies') {
            steps {
                bat 'npm install'
            }
        }
        
        stage('Build') {
            steps {
                bat 'npm run build'
            }
        }
        
        stage('Test') {
            steps {
                bat 'npm test'
            }
        }
        
        stage('Deploy') {
            steps {
                bat 'npm start'
            }
        }
    }
}

