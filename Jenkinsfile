pipeline {
    agent any
    stages {
        stage('Deploy') {
            steps {
                withCredentials([sshUserPrivateKey(credentialsId: 'root', keyFileVariable: 'SSH_KEY_FILE', passphraseVariable: 'SSH_PASSPHRASE', usernameVariable: 'SSH_USER')]) {
                    sshagent(['root']) {
                        sh 'ssh -i $SSH_KEY_FILE $SSH_USER@localhost "echo Hello, world!" > /tmp/test'
                    }
                }
            }
        }
    }
}

