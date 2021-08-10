pipeline {
    agent { dockerfile true }
    parameters {
        string (name: 'NAME', defaultValue: 'mypage', description: 'Please wtite your image name')
    }
    environment {
        NAME = 'mypage'
    }
    stages {
        stage ('BuildImage') {
            agent {         
               docker {          
                  docker.image('876d21596a72').withRun('-p 8888:80')
                  label 'custom'				  
               }
            }
        }             
            
            steps {
                  echo "Finish"            
            }
    }     
}
