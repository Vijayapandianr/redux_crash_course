pipeline {
    agent  {
         label 'sam_node'
    }

    stages {
        
        stage ('Checkout') {
            steps {
                checkout scm
                }
            }
        stage('Build') { 
            steps {
                bat 'npm install' 
            }
        }   
        
        stage('Start the App') { 
            steps {
                bat 'npm start' 
            }
        }   
        stage ('Testing') {
            steps {
                bat 'npm run test'
                }
            }
        stage ('Deployment Build'){
            steps {
               bat 'npm run build'
            }
        }
    }
}
