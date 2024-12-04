pipeline {
    agent any
    
    stages {
        stage ('Build w/o docker') {
            steps {
                sh '''
                    echo "Working without docker"
                    touch woContainer.txt
                '''   
            }
        }
        stage('Build w/docker') {
            agent {
                docker {
                    image 'node:18-alpine'
                }
            }
            steps {
                sh '''
                    ls -la
                    touch dockerContainer.txt
                    ls -la
                '''
            }
        }
    }
}
