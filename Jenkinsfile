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
               bat "dotnet publish  --configuration Release"
            }          
        }
        stage("Run tests"){            
            steps{
                bat " dotnet test --no-build --verbosity normal"
            }          
        }
    }
   
}
