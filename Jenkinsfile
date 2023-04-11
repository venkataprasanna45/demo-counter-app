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
        stage ('Build & JUnit Test') {
            steps {
                sh 'mvn install' 
            }
            post {
               success {
                    junit 'target/surefire-reports/**/*.xml'
                }   
            }
        }
        stage('Static code analysis'){
            
            steps{
                
                script{
                    
                    stage('Static code analysis'){
            
            steps{
                
                script{
                    
                    withSonarQubeEnv(credentialsId: 'sonar-api') {
                        
                        sh 'mvn clean package sonar:sonar'
                    }
                   }
                    
                }
            } {
                        
                        sh 'mvn clean package sonar:sonar'
                    }
                   }
                    
                }
            }
    

           
    }
}