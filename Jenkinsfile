pipeline {
    agent {
        docker {
            image 'python:3.9'  // Verwende ein Docker-Image mit Python und pip vorinstalliert
        }
    }
    stages {

        stage('Checkout') {
            steps {
                git url: 'https://github.com/rimat420/jenkins-project.git', branch: 'main'
                sh "ls -ltr"
            }
        }
        stage('Setup') {
            steps {
                sh "pip install -r requirements.txt"
            }
        }
        stage('Test') {
            steps {
                sh "pytest"
                sh "whoami"
            }
        }
        
    }
}
