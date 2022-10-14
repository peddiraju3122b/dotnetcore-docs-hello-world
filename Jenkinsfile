pipeline{
    agent{label 'jdk11'}
    stages{
        stage(dotnetapp){
            steps{
                git url:'https://github.com/GitPracticeRepo/dotnetcore-docs-hello-world.git',
            branch: 'master'
            }
        
        }
        stage(dotnetbuild){
            steps{
                sh """dotnet build dotnetcoresample.csproj
                    dotnet publish dotnetcoresample.csproj
                    zip -r dotnetcore-docs-hello-world-1.0.0.zip /home/ubuntu/dotnetcore-docs-hello-world/bin/Debug/net6.0/publish"""
            }
        }
    
    }
}