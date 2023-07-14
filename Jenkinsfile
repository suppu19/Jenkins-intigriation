pipeline{
agent any 
    stages{
    stage('test') {
        steps{
        echo 'Knowledge Is Free'
    
        echo "=======================================Checking Out Code from Github======================================="
    }  
    }    
       
       
   
    
   
    stage('Maven Build') {
         steps{   
            sh "mvn clean package"

       
    
    }
}
    }
}
