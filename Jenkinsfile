pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    buildImage()
                }
            }
        }
    }
}

def buildImage(){
    sh "docker build -t tsnetkovs/api-tests:latest ."
    sh "docker push tsnetkovs/api-tests"
}