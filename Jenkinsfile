pipeline{
    agent any

    stages {

        stage('Build docker image') {
            steps {
                script {
                    dockerapp = docker.build("guilhermeolii/kube-news:${env.BUILD_ID}", '-f ./src/dockerfile ./src')
                }
            }
        }

        stage('Push docker image') {
            steps {
                script {
                    docker.withRegistry('https://registry.hub.docker.com', 'dockerhub') {
                        dockerapp.push('latest')
                        dockerapp.push("${env.BUILD_ID}")
                    }
                }
            }
        }
    }
}