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
            steps {
              docker.image($(NAME)).withRun('-p 8888:80')
            }
        }
   }    
}
