pipeline {
    agent any

    stages {
        stage('Git Stage') {
            steps {
                git branch: 'main', url: 'https://github.com/wasdqaz/MMT-22127210-devops.git'
            }
        }

        stage('Build and Push Docker Image'){
            steps {
                withDockerRegistry(credentialsId: 'docker-hub-22127210', url: 'https://index.docker.io/v1/') {
                    sh 'docker build -t 22127210/devops .'
                    sh 'docker push 22127210/devops'  
                }
            }
        }
    }
}
