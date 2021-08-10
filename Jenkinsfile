pipeline {
    agent { dockerfile true 
        docker{
            label 'custom'
        }
    }
    parameters {
        string (name: 'LABEL', defaultValue: 'mypage', description: 'Please wtite your image name')
    }
    environment {
        NAME = 'mylabel'
    }
    stages {
        stage ('BuildImage') {
            steps {
               echo "Finish"
            }
        }
   }     
}
