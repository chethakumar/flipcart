pipeline {
    agent any

    stages {
        stage('pull the image') {
            steps {
                sh 'sudo docker pull nginx'
            }
        }

        stage('run the container') {
            steps { 
                 sh 'docker stop nginx'
                 sh ' docker rm nginx'
                 sh 'sudo docker run -it -d --name app -p 80:80 nginx'
            }
        }
    }
}
