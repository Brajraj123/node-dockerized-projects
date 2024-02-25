pipeline {
    agent any
    tools {
        nodejs 'NodeJS'
    }
    stages {
        stage("Test") {
            steps {
                sh 'npm test'
            }
        }
        stage("Build") {
            steps {
                sh 'npm run build'
            }
        }
        
        stage("Build Docker Image") {
            steps {
                sh 'sudo docker build -t my-node-app:1.0 .'
            }
        }
    }
}
