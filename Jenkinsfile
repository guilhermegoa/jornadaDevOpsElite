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

        stage('Deploy k8s') {
            steps {
                enviroment {
                    tag_version = "${env.BUILD_ID}"
                }
                withKubeConfig([credentialsId: 'kubeconfig']) {
                    sh 'seed -i "s/{{TAG}}/$tag_version/g" ./k8s/deployment.yaml'
                    sh 'kubectl apply -f ./k8s/deployment.yaml'
                }
            }
        }
    }
}