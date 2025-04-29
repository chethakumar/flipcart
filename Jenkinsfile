pipeline {
    agent any

    stages {
        stage('pull the image') {
            steps {
                sh 'sudo docker pull nginx'
            }
        }

        stage('stop the container') {
            steps { 
                 sh 'docker stop nginx'
            }
        }
      stage('remove the container') {
            steps { 
             sh ' docker rm nginx' 
            }
      }
        stage('to run docker'){
            steps{
                sh 'docker run -it -d --name app -p 80:80 nginx'
            }
        }
                 
    }
}
