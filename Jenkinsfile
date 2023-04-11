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
    }
}