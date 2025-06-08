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
    git "https://github.com/Timsons/api-tests-final.git"
    sh "docker build -t tsnetkovs/api-tests:latest ."
    sh "docker push tsnetkovs/api-tests:latest"
}