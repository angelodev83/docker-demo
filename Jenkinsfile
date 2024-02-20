pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    // Build Docker image
                    dockerImage = docker.build('docker-nodejs:latest)

                    // Push Docker image to a registry
                    docker.withRegistry('https://hub.docker.com/r/angeloti83/docker-nodejs-demo', 'angeloti83') {
                        dockerImage.push()
                    }
                }
            }
        }
    }
}
