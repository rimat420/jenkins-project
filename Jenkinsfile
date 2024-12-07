pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/420/jenkins-project.git', branch: 'main'
                sh 'ls -ltr'
            }
        }
        
        stage('Setup') {
            steps {
                script {
                    docker.image('python:3.9').inside {
                        sh 'pip install -r requirements.txt'
                    } // Ende von docker.image().inside
                } // Ende von script
            } // Ende von steps
        } // Ende von stage 'Setup'
        
        stage('Test') {
            steps {
                sh 'pytest'
                sh 'whoami'
            } // Ende von steps
        } // Ende von stage 'Test'
        
    } // Ende von stages
} // Ende von pipeline
