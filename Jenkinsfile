pipeline{
    agent any
    stages{
        stage("Build and Test"){
            steps{
                sh "docker build . -t node-app:latest"
            }
        }
        stage("Deploy"){
            steps{
                sh "docker-compose down && docker-compose up -d"
            }
        }
    }
}
