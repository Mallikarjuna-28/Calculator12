pipeline {
    agent any
    
    tools {
        jdk 'jdk17'   // Make sure JDK is configured in Jenkins
    }

    stages {

        stage('Clone') {
            steps {
                git branch: 'main', 
                    url: 'https://github.com/Mallikarjuna-28/Jenkinsjavaparam.git'
            }
        }

        stage('Compile') {
            steps {
                sh 'javac Calculator.java'
            }
        }

        stage('Build') {
            steps {
                sh 'java Calculator 25 5'
            }
        }

        stage('Test') {
            steps {
                sh 'java Calculator 30 -5'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment completed'
            }
        }
    }

    post {
        success {
            echo 'Pipeline executed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
