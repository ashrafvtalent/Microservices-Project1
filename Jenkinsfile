pipeline {
agent {
label 'build-server '
}

stages {

stage ('Checkout') 
{
steps
    {
    
        checkout scm
        
    }
    
}
stage ('Build1') 
{
    steps
    {
       sh "cd /home/ubuntu/workspace/JenkinsPipelineDevops/account-service ; mvn clean install " 
    }
}
  stage ('dockerbuild') 
{
    steps
    {
       sh "cd /home/ubuntu/workspace/JenkinsPipelineDevops/account-service ; sudo docker build -t account-service ."
        
    }
}
       
} 
}  
