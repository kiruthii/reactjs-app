pipeline {
    agent any
  

    stages {
        stage('Git Checkout') {
            steps {
                git url:'https://github.com/kiruthii/reactjs-app.git',branch:"main"
            }
        }
        stage('NPM install') {
            steps {
                bat "npm install"
            }
        }
        stage('Build') {
            steps {
                bat "npm run build"
            }
        }
        stage('Vercel Deploy') {
            steps {
                bat 'curl -v -X POST https://api.vercel.com/v1/integrations/deploy/prj_xMQjTm0VAIqLu1GHoyhTGalKvIfo/9uP0Zhcrc6'

            }
        }
        
    }
}
