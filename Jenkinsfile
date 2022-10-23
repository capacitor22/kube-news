pipeline{
    // como a maquina do agente é a mesma, posso usar any abaixo
    agent any 

    stages {

        stage ('Build docker image') {
            steps{
                script {
                    dockerapp = docker.build("capacitor22/kube-news:${env.BUILD_ID}", '-f ./src/Dockerfile ./src')
                }
            }
        }
    }
}