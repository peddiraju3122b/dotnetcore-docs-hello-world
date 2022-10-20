pipeline{
    agent{label 'dotnetjdk11'}
    stages{
        stage('gitclone'){
            steps{
                git url : 'https://github.com/GitPracticeRepo/dotnetcore-docs-hello-world.git',
                branch : 'master'
            }
        }
        stage('dotnetbuild'){
            steps{
                sh 'dotnet build dotnetcoresample.csproj'
            }
        }
        stage('dotnetpublish'){
            steps{
                sh 'dotnet publish dotnetcoresample.csproj'
            }
        }
        stage('unzipfile'){
            steps{
                sh 'zip -r dotnetcore-docs-hello-world-1.0.0.zip /home/ubuntu/dotnetcore-docs-hello-world/bin/Debug/net6.0/publish'
            }
        }
    }
}