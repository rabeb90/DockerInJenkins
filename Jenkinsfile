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
             
                bat 'docker run jenkins:2.60.3'             
          }
        }
    }
}
