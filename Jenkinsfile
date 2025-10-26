pipeline{
    agent any
    stages{
        stage("Restore .Net Packages"){
            steps{
                bat 'dotnet restore' //for windows
            }
        }
        stage("Build .Net Project"){
            steps{
                bat 'dotnet build --no-restore' //for windows
            }
        }
        stage("Run .Net Unit and Integration Tests"){
            steps{
                bat 'dotnet test --no-build --verbosity normal' //for windows
            }
        }
    }
}