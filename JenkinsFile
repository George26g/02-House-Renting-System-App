pipeline{
    agent any


    stages{
        stage('Checkout'){
            steps{
                git branch: 'main', url: "https://github.com/George26g/02-House-Renting-System-App"
            }
        }

        stage("Restore dependences"){
            steps{
                script{
                  
                    bat 'dotnet restore'
                }
            }
        }
        stage("Build application")
        {
            steps{
                script{
                    bat 'dotnet build'
    
                }
            }
        }
         stage("run tests")
        {
            steps{
                script{
                    bat 'dotnet test'
                    
                }
            }
        }
    }

    post {
        always{
            echo "CI pipeline completed"
        }
    }
}