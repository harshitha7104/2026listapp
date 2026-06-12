pipeline {
    agent any
    tools { maven 'Maven' }
    
    stages {
        stage('Checkout') {
            steps {
                // This automatically reads the repo details from your Jenkins job configuration page
                checkout scm 
            }
        }
        stage('Build & Test') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage('Run Application') {
            steps {
                sh 'java -jar target/2026listapp-1.0-SNAPSHOT.jar'
            }
        }
    }
}
