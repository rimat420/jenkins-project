pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/rimat420/jenkins-project.git', branch: 'main'
                sh 'ls -ltr'
		sh 'pwd'
            }
        }
        
        stage('Setup') {
            steps {
                sh '''
                    python3 -m venv venv
                    . venv/bin/activate
                    pip install -r requirements.txt
                '''
            }
        }        
        
        stage('Test') {
            steps {
                        sh '''
                            . venv/bin/activate
                            pytest
                        '''
                // sh 'pytest'
                // sh 'whoami'
            } // Ende von steps
        } // Ende von stage 'Test'
        
    } // Ende von stages
} // Ende von pipeline
