pipeline {
    agent any

    environment {
        DATE = new Date().format('yy.M')
        TAG = "${DATE}.${BUILD_NUMBER}"
    }

    stages {
        stage ('Build') {
            steps {
                echo "Command to check out code from github to come here"
                echo "${TAG}"
            }
        }
        stage ('Docker Build'){
            steps {
                script {
                    docker.build("nravinuthala/myapp:${TAG}")
                }
            }
        }
        stage ('Pushing to Docker Hub'){
            steps {
                script {
                    docker.withRegistry('https://registry.hub.docker.com', 'docker-hub-creds'){
                        docker.image("nravinuthala/myapp:${TAG}").push()
                        docker.image("nravinuthala/myapp:${TAG}").push("latest")
                    }
                }
            }
        }
    }
}