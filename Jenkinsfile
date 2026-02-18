pipeline{
    agent any
    stages{
        stage("Restore dep."){
            when {
                anyOf{
                    branch 'main'
                    branch 'feature'
                }
            }
            steps{
                bat "dotnet restore"
            }          
        }
        stage("build App"){
            when {
                anyOf{
                    branch 'maim'
                    branch 'feature'
                }
            }
            steps{
                bat "dotnet build --no-restore"
            }          
        }
        stage("Run tests"){
            when {
                anyOf{
                    branch 'maim'
                    branch 'feature'
                }
            }
            steps{
                bat " dotnet test --no-build --verbosity normal"
            }          
        }
    }
   
}