pipeline {
    agent any 
    stages {
        stage('Git Clone ') {
            steps {
                git credentialsId: 'b6513267-59ef-425c-8e59-d55f0028ff9e', url: 'https://github.com/prakashraju619/sample-nodejs-app.git' 
            }
        }
    }

    stages {
        stage('Docker file creating') {
            steps {
                sh "docker build  -t node-jk-app . "
                sh" docker run -d -p 7000:4000 --name node-jp-conc" 
                
            }
        }
    }
}
