pipeline {
    agent any
 stages {
      stage('checkout') {
           steps {
             
                git branch: 'master', url: 'https://github.com/rabeb90/DockerInJenkins.git'
             
          }
        }
  stage('Run Docker Container on Jenkins') {
           steps {
             
                run 'docker run integrate-docker-jenkins'             
          }
        }
    }
}
