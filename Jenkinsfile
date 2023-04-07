pipeline {

    agent any 

    stages {

        stage("git checkout"){
            
            steps{
                git branch: 'main', url: 'https://github.com/venkataprasanna45/demo-counter-app.git'
            }
         }
         stage("UNIT TESTING"){
            
            steps{
                sh "mvn test"
            }
         }
    }
}