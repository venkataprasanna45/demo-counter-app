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
         stage("UNIT TESTING"){
            
            steps{
                sh'mvn test'
            }
         }
         stage("Integration testing"){
            
            steps{
                sh'mvn verify-DskipunitTests'
            } 
    }
}