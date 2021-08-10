pipeline {
    agent {dockerfile {
             filename 'Dockerfile'
          }
    }       
    parameters {
        string (name: 'LABEL', defaultValue: 'mylabel', description: 'Please wtite your label name')
    }
    environment {
        LABEL = 'mylabel'
    }
    stages {
        stage('Initialize'){
           def dockerHome = tool 'myDocker'
           env.PATH = "${dockerHome}/bin:${env.PATH}"
        }
        stage ('RunImage'){
            steps {
               sh 'docker run -d -p 8888:80 876d21596a72'
               echo "Finish"
            }
        }
   }     
}
