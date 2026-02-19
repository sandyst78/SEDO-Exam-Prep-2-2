pipeline{
    agent any
    stages{
        stage("Restore dep."){           
            steps{
                bat "dotnet restore"
            }          
        }
        stage("build App"){            
            steps{
               bat "dotnet publish  --no-restore"
            }          
        }
        stage("Run tests"){            
            steps{
                bat " dotnet test --no-build --verbosity normal"
            }          
        }
    }
   
}
