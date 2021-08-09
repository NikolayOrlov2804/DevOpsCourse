pipeline {
    agent any
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
                docker run -it --rm -d -p 8080:80 --name ${WEB} ${NAME}

              '''
            }
        }
   }    
}
