pipeline {

    agent any 
    tools{
        maven "maven"
    }

    stages {

        stage("git checkout"){
            
            steps{
                git branch: 'main', url: 'https://github.com/venkataprasanna45/demo-counter-app.git'
            }
         }   
        stage('UNIT testing'){
            
            steps{
                
                script{
                    
                    sh 'mvn test'
                }
            }
        }    
    }
}