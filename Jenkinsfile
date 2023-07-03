pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout the source code from your repository
                checkout scm
            }
        }
        
        stage('Restore') {
            steps {
                // Restore NuGet packages
                bat 'nuget restore'
            }
        }
        
        stage('Build') {
            steps {
                // Build the .NET project
                bat 'dotnet build'
            }
        }
        
        stage('Test') {
            steps {
                // Run tests
                bat 'dotnet test'
            }
        }
        
        stage('Publish') {
            steps {
                // Publish the project
                bat 'dotnet publish -c Release -o ./publish'
            }
        }
    }
}
