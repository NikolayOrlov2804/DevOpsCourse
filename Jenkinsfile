pipeline {
    agent {dockerfile {
             filename 'Dockerfile'
             label "${LABEL}"
           }
    }       
    parameters {
        string (name: 'LABEL', defaultValue: 'mylabel', description: 'Please wtite your label name')
    }
    environment {
        LABEL = 'mylabel'
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
