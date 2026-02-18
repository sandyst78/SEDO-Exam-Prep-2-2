pipeline{
    agent any
    stages{
        stage("Restore dep."){
            when {
                anyOf{
                    branch 'main'                    
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
                }
            }
            steps{
                bat " dotnet test --no-build --verbosity normal"
            }          
        }
    }
   
}
