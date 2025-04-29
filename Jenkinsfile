pipeline {
    agent any

    stages {
        stage('pull the image') {
            steps {
                sh 'sudo docker pull nginx'
            }
        }

        stage('stop the container if exists') {
            steps { 
                sh 'sudo docker stop app || true'
            }
        }

        stage('remove the container if exists') {
            steps { 
                sh 'sudo docker rm app || true'
            }
        }

        stage('run the container') {
            steps {
                sh 'sudo docker run -it -d --name app -p 80:80 nginx'
            }
        }
    }
}
