pipeline {
    agent any

    tools {
        maven 'Maven'   // configure in Jenkins tools
    }

    stages {

       

        stage('Build') {
            steps {
                bat 'mvn clean compile'
            }
        }

        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }

        stage('Package') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
