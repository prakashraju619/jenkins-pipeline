pipeline {
    agent any 
    stages {
        stage('Git Clone') {
            steps {
                git branch: 'main', credentialsId: 'b6513267-59ef-425c-8e59-d55f0028ff9e', url: 'https://github.com/prakashraju619/sample-nodejs-app.git' 
            }
        }

    stage('Building image') {
      steps{
        script {
           docker build -t node-app-img .

        }
      }
    }

    stage('Deploy Run') {
      steps{
        script {
         docker run -d -p 6000:4000 --name node-app-conc node-app-image

          }
        }
      }
    }

    }



   
   
    
      



