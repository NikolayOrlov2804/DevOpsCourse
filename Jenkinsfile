pipeline {
    agent {dockerfile true}   
      stages {
        stage('RunImage') {
            steps {
                sh 'docker run -d -p 8888:80 876d21596a72'
            }
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
