pipeline {
    agent any

    tools {
        maven 'Maven'   // configure in Jenkins tools
    }

    stages {

        stage('Clone Code') {
            steps {
                git 'https://github.com/your-username/your-project.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean compile'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Package') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
