pipeline {
    agent any
    stages{
        stage("Clone Code"){
            steps{
                git url: "https://github.com/kelvinmanavar/node-app-jenkins.git", branch: "master"
            }
        }
        stage("Build and Test"){
            steps{
                sh "docker build . -t node-app-test-new"
            }
        }
        stage("Deploy"){
            steps{
                sh "sudo docker-compose down && sudo docker-compose up -d"
            }
        }
    }
}
