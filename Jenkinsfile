pipeline {
 environment{
  dockerImage=""
 }
  agent any
  stages {
    stage('Cloning Git') {
      steps {
        git branch: 'main', credentialsId: 'b6513267-59ef-425c-8e59-d55f0028ff9e', url: 'https://github.com/prakashraju619/sample-nodejs-app.git' 

      }
    }
    stage('Building image') {
      steps{
        script {
          dockerImage =  docker . build 
        }
      }
    }
   
    }
    
  }
