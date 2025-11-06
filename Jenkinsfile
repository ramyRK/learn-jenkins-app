pipeline {
    agent any

    stages {
        stage('Build') {
            agent{
                image 'node:18-alpine'
                reuseNode true
            }
            steps {
                sh'''
                ls -la
                node --version
                npm --vesrion
                npm ci
                npm run build
                ls -ls
                '''
            }
        }
    }
}
