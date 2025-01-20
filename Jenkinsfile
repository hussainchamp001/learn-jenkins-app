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
                }
            }
            steps {
                sh 'npm --version'
            }
        }
    }
}
