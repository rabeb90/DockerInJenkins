pipeline {
    agent any
 stages {
      stage('checkout') {
           steps {
             
                git branch: 'main', url: 'https://github.com/rabeb90/DockerInJenkins.git'
             
          }
        }
  stage('Run Docker Container on Jenkins') {
           steps {
             
                sh 'docker run integrate-docker-jenkins'             
          }
        }
 stage('Run Docker container on remote hosts') {
             
            steps {
                sh "docker -H ssh://jenkins@172.31.28.25 run integrate-docker-jenkins"
 
            }
        }
    }
}
