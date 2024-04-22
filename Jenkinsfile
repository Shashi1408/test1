pipeline {
    agent none 
    
    stages {
        
        stage('Build') {
            steps {
                sh 'rm -rf test1;git clone https://github.com/Shashi1408/test1.git'
            }
        }
        
        stage('Deploy') {
            steps {
                sh 'cd test1 ; python3 s2.py > /tmp/s2'
            }
        }
    }
}
