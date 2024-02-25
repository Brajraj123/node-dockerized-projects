pipeline {
    agent any
    stages {
        stage("Checkout") {
            steps {
                checkout scm
            }
        }

        stage("Test") {
            steps {
                script {
                    // Install npm using Jenkins tool directive
                    tool name: 'npm', type: 'npm'
                    sh 'npm test'
                }
            }
        }

        stage("Build") {
            steps {
                script {
                    // Install npm using Jenkins tool directive
                    tool name: 'npm', type: 'npm'
                    sh 'npm run build'
                }
            }
        }
    }
}
