pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/rimat420/jenkins-project.git', branch: 'main'
                sh 'ls -ltr'
            }
        }
        
        stage('Setup') {
            steps {
                sh "pip install -r requirements.txt"
            }
        }        
        
        stage('Test') {
            steps {
                sh 'pytest'
                sh 'whoami'
            } // Ende von steps
        } // Ende von stage 'Test'
        
    } // Ende von stages
} // Ende von pipeline
