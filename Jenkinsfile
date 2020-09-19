pipeline {
    
    agent any
    
    stages {
        stage("preparding environment"){
            
            steps{
                
                echo 'cloning the repo'
                git 'https://github.com/buildkite/python-docker-example.git'
                echo 'cloned the repo'
            }
        }
        stage("building docker"){
            
            steps{
                
                echo 'directory list'
                sh label: '', script: 'docker build .'
            }
        }
        stage("listing the docker images"){
            
            steps{
                
                echo 'docker images'
                sh label: '', script: 'docker images'
                sh label: '', script: 'docker ps'
            }
        }
    }
    
}