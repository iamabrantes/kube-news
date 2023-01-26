pipeline {
    agent any

    stages{
        stage ('Build Docker Image'){
            steps{
                script{
                    dockerapp = docker.build("jonathanabrantes/kube-news:v1", '-f ./src/Dockerfile ./src')
                }
            }
        }

    }


}