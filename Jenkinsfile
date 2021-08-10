pipeline {
    agent {dockerfile true}              
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
