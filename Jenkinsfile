node {
    stage('test') {
        echo 'Knowledge Is Free'
    }
        echo "=======================================Checking Out Code from Github======================================="
       
        stage('Git Checkout') {
       
        git branch: 'main', credentialsId: 'Github', url: 'https://github.com/suppu19/project1.git'
       
        echo "=======================================Pulled Code from Github======================================="   
    }
   
    echo "=========================================Building Maven Project=========================================="
   
    stage('Maven Build') {
       
            sh "mvn clean package"

       
    
    }
}
