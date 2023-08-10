pipeline {    
  agent any        
  stages{        
    stage('checkout') {            
      steps{              
        git branch: 'main', changelog: false, poll: false, url: 'https://github.com/chandanko/Jenkins.git'            
           }        
       }        
    stage ('Docker build'){            
      steps{                
        script{                    
          withDockerRegistry(credentialsId: 'Docker_id') {                     
            sh "docker build -t image_name"                    
            sh "docker push"                    
          }                                    
        }            
      }        
    }    
  }
}
