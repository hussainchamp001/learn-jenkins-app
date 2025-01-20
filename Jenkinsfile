pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                sh 'npm --version'
            }
        }
        stage('Using Docker') {
            agent {
                docker {
                    image 'node:18-alpine'
                    reuseNode true
                }
            }
            steps {
                sh '''
                    ls -la
                    npm --version
                    node --version
                    npm ci
                    npm run build
                    ls -la
                '''    
            }
        }
    }
}
