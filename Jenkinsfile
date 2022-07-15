pipeline {
    agent any 
    stages {
        stage('Git Clone ') {
            steps {
               git branch: 'main', credentialsId: 'b6513267-59ef-425c-8e59-d55f0028ff9e', url: 'https://github.com/prakashraju619/sample-nodejs-app.git'
            }
        }
		stage('Docker file creating') {
            steps {
              
		 sh "sudo systemctl start docker"
		 sh "docker build  -t node-jk-app . "
                sh" docker run -d -p 7000:4000 --name node-jp-conc" 
               
                
                
            }
        }

		
    }

    
       
}
