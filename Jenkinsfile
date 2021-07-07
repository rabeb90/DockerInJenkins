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
             
                sh 'docker run integrate-docker-jenkins'             
          }
        }
     stage('Push image') {
        docker.withRegistry('https://registry.hub.docker.com', 'git') {            
       app.push("${env.BUILD_NUMBER}")            
       app.push("latest")        
              }    
           }
    }
}
