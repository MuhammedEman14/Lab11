pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout code from GitHub repository
                git 'https://github.com/MuhammedEman14/Lab11'
            }
        }
        
        stage('Dependency Installation') {
            steps {
                // Install dependencies for the frontend
                bat 'npm install' 
            }
        }
        
        stage('Build Docker Image') {
            steps {
                // Build Docker image
                bat 'docker build -t myapp:latest .'
            }
        }
        
        stage('Run Docker Image') {
            steps {
                // Run Docker image
                bat 'docker run -d -p 8080:80 myapp:latest' 
            }
        }
        
        stage('Push Docker Image') {
            steps {
                // Push Docker image to Docker Hub
                
                    bat 'docker push myapp:latest'
                }
            }
        }
    }

