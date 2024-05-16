pipeline {
    agent any
    stages  {
        stage (checkout) {
            steps {
                checkout scmGit(branches: [[name: '**']], extensions: [], userRemoteConfigs: [[credentialsId: 'c644c3c7-3907-4f86-bb58-b6cdd796aaf4', url: 'https://github.com/halyaks/Demo']])
            }
        }
        stage (test) {
                steps {
                sh 'python tests/test.py'
            }
        }
    }
}

