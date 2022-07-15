pipeline {
 
  agent any
  stages {
    stage('Cloning Git') {
      steps {
        git branch: 'main', credentialsId: 'b6513267-59ef-425c-8e59-d55f0028ff9e', url: 'https://github.com/prakashraju619/sample-nodejs-app.git' 

      }
    }

    stage('Image Build') {
      steps {
        script {
            sh 'docker build -t nodeapp-1 .'
        }

      }
    }

    stage('Docker  Run') {
      steps {
        script {
            sh 'docker run -d  -p 3000:3000 nodeapp-1'
        }

      }
    }
   
   
    }
    
  }
