pipeline {
    agent any

    stages {
        
        stage('Build') {
            steps {
                sh 'git clone https://github.com/Shashi1408/test1.git'
            }
        }
        
        stage('Deploy') {
            steps {
                sh 'cd test1 ; python3 s2.py > /tmp/s2'
            }
        }
    }
}
