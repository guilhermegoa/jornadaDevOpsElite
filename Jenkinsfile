pipeline{
    agent any

    stages {

        stage('Build docker image') {
            steps {
                script {
                    dockerapp = docker.build("guilhermeolii/kube-news:${env.BUILD_ID}", '-f ./src/Dockerfile ./src')
                }
            }
        }
    }
}