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
                script {
                    docker.build("my-node-app:1.0")
                }
            }
        }
    }
}
