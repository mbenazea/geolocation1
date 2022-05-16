pipeline {
   triggers {
       pollSCM('* * * * *')
    } 
   agent any
    tools {
        maven 'M2_HOME'
    }
    stages {
        stage('maven package') {
            steps {
                sh 'mvn clean'
                sh 'mvn install'
                sh 'mvn package'
               }
        }
        stage('Test') {
            steps {
                 sh 'mvn test'   
            }
        }
        stage('Deloy') {
            steps {
                echo 'Deploy'       
            }
        }
        stage('Docker') {
            steps {
                echo 'Docker step'             
            }
        }
    }

}

