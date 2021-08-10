pipeline {
    agent {dockerfile {
             filename 'Dockerfile'
             label 'my-defined-label'
           }
    }       
    parameters {
        string (name: 'LABEL', defaultValue: 'mypage', description: 'Please wtite your label name')
    }
    environment {
        NAME = 'mylabel'
    }
    stages {
        stage ('RunImage') {
            steps {
               sh 'docker run -d -p 8888:80 876d21596a72'
               echo "Finish"
            }
        }
   }     
}
