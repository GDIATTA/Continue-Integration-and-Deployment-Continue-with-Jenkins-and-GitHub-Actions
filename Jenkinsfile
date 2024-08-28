pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                git changelog: false, poll: false, url: 'https://github.com/GDIATTA/CI_CD.git' 
            }
        }
        stage('Test1') { 
            steps {
                sh 'python3 --version'
                sh 'ls'
            }
        }
        stage('Test2') { 
            steps {
                sh '''
                
                    set -e
                    python3 -m venv venv
                    . venv/bin/activate
                    pip install --upgrade pip --break-system-packages
                    pip install pytest
                    pytest test_pytest.py
                    deactivate
                '''
            }
        }

    }
}
