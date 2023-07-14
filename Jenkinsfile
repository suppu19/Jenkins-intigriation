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

                
        stage("sonarqube"){
            steps {
                script {
                    withSonarQubeEnv(credentialsId: 'newsonar-tocken') {
                        sh "mvn sonar:sonar"
                        }

                }
            }
        }

        
    } 
     
     
     //    stage ("s3-upload"){
    //              entries: [
    //                 [bucket: 'maven-web-application',
    //                  excludedFile: '',
    //                  flatten: false,
    //                  gzipFiles: false,
    //                  keepForever: false,
    //                  managedArtifacts: false,
    //                  noUploadOnFailure: false,
    //                  selectedRegion: 'ap-south-1',
    //                  showDirectlyInBrowser: false,
    //                  sourceFile: '*/target/.war',
    //                  storageClass: 'STANDARD',
    //                  uploadFromSlave: false,
    //                  useServerSideEncryption: false]
    //                 ], pluginFailureResultConstraint: 'FAILURE',
    //                    profileName: 'maven-web-application',
    //                    userMetadata: []
    //             }
    //         }
    //     }
    }

