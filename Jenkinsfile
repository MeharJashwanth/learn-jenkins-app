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
                sh ''''
                    npm run build
                '''
            }
        }
        stage('Test') {
            steps{
                sh '''
                    echo "Test stage"
                '''
            }
        }
    }
}
