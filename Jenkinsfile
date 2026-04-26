pipeline {
    agent any

    tools {
        maven 'maven3'   // must match Jenkins tool config exactly
        jdk 'jdk21'
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
                bat 'mvn package'
            }
        }

        stage('Run Application') {
            steps {
                bat '''
                    echo Starting application...
                    taskkill /F /IM java.exe /T || exit 0
                    start java -jar target\\*.jar
                '''
            }
        }
    }
}
