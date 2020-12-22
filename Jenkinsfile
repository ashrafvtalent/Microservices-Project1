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
    stage ('dockerimagepush') 
{
    steps
    {
       sh "cd /home/ubuntu/workspace/JenkinsPipelineDevops/account-service ; sudo  docker login -uashrafdoc -pAlibeta@123"
       sh "cd /home/ubuntu/workspace/JenkinsPipelineDevops/account-service ; sudo docker tag account-service ashrafdoc/account-service"
       sh "cd /home/ubuntu/workspace/JenkinsPipelineDevops/account-service ; sudo docker push ashrafdoc/account-service"
        
        
    }
}
    
} 
}  
