pipeline {
    agent {
     label '172.31.29.115'
    }
    
    agent {
     label '172.31.19.156'
    }

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
