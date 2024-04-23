pipeline {
    agent any

    environment {
        SERVERS = ['172.31.22.238', '172.31.23.202'] // List of servers to deploy to
        USERNAME = 'ec2-user' // SSH username
        REMOTE_DIR = '/home/ec2-user' // Remote directory to deploy to
        LOCAL_DIR = '/home/ec2-user' // Local directory containing files to deploy
    }

        stage('Deploy') {
            steps {
                script {
                    // Loop through each server
                    for (server in env.SERVERS) {
                        // Deploy using SSH
                        sshagent(credentials: [env.SSH_KEY]) {
                            sh "python3 s2.py > /tmp/s2"
                        }
                    }
                }
            }
        }
    }
 }
}

