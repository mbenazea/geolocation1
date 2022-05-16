pipeline {

    agent any
    tools {
        maven 'M2_HOME'
    }

    triggers {
        pollSCM '* * * * *'
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
                sleep 5
            }
        }
        stage('Deloy') {
            steps {
                echo 'Deploy'
                sleep 5
            }
        }
        stage('Docker') {
            steps {
                echo 'Docker step'
                sleep 5
            }
        }
    }

}

