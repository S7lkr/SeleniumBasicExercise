pipeline {
    agent any
    stages {
        stage('Restore dependencies') {
            steps {
                bat 'dotnet restore'
            }
        }
        stage('Build Project') {
            steps {
                // Commands to build
                bat 'dotnet build --configuration Release'
            }
        }
        stage('Run dotnet UI tests for Project 1') {
            steps {
                bat 'dotnet test TestProject1/TestProject1.csproj --no-build --verbosity normal'
            }
        }
        
        stage('Run dotnet UI tests for Project 2') {
            steps {
                bat 'dotnet test TestProject2/TestProject2.csproj --no-build --verbosity normal'
            }
        }
        
        stage('Run dotnet UI tests for Project 3') {
            steps {
                bat 'dotnet test TestProject3/TestProject3.csproj --no-build --verbosity normal'
            }
        }
    }
}
