pipeline {
    agent any

    stages {
        stage('Build') {
            agent {
                docker {
                    image 'node:18-alpine'
                    reuseNode true
                }
            }
            steps {
                echo 'Building Learn-Jenkins-App...'
                sh '''
                    ls -a
                    node --version
                    npm --version
                    npm ci
                    npm run build
                    ls -a
                '''
            }
        }
    }
}
