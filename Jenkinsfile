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
              sh '''
                docker build -t ${NAME} .
                docker run -d -p 8888:80 ${NAME}

              '''
            }
        }
   }    
}
