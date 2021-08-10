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
              sudo docker run -d -p 8888:80 876d21596a72
              echo "Finish"
            }
        }
   }    
}
