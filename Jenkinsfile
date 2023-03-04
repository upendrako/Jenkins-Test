pipeline {
    agent any
    stages {
        stage('Deploy') {
            steps {
                withCredentials([sshUserPrivateKey(credentialsId: 'myown', keyFileVariable: 'SSH_KEY_FILE', passphraseVariable: 'SSH_PASSPHRASE', usernameVariable: 'SSH_USER')]) {
                    sshagent(['myown']) {
                        sh 'ssh -i $SSH_KEY_FILE $SSH_USER@localserver "echo Hello, world!" > /tmp/test'
                    }
                }
            }
        }
    }
}

