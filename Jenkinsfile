pipeline {
    agent any
    stages {
        stage('Deploy') {
            steps {
                sshagent(credentials:['root']){
                sh 'ssh  -o StrictHostKeyChecking=no  root@192.168.0.115 uptime "whoami"'
                    }
                }
            }
        }
    }
}

