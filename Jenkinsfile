pipeline{
    agent any
    stages{
        stage("Restore .Net Packages"){
             when {
                branch 'main'
            }
            steps{
                bat 'dotnet restore' //for windows
            }
        }
        stage("Build .Net Project"){
             when {
                branch 'main'
            }
            steps{
                bat 'dotnet build --no-restore' //for windows
            }
        }
        stage("Run .Net Unit and Integration Tests"){
             when {
                branch 'main'
            }
            steps{
                bat 'dotnet test --no-build --verbosity normal' //for windows
            }
        }
    }
}