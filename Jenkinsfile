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
       sh "cd /home/ubuntu/workspace/JenkinsPipelineJob/account-service ; mvn clean install " 
    }
}
} 
}  