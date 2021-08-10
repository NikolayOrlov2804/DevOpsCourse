pipeline {
    agent {dockerfile true}
    parameters {
        string (name: 'LABEL', defaultValue: 'mylabel', description: 'Please wtite your label name')
    }
    environment {
        LABEL = 'mylabel'
    }
    stages {
         stage ('RunImage'){
            steps {
               echo "Finish"
            }
        }
   }     
}
