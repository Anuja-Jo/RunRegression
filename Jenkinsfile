pipeline {
    agent any

    tools {
        maven 'Maven'   // configure in Jenkins tools
    }

    stages {

        stage('Clone Code') {
            steps {
                git 'https://github.com/Anuja-Jo/RunRegression.git'
            }
        }

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
