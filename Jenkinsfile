pipeline {
    agent any
    tools {
        nodejs 'name_of_nodejs_installation'
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
    }
}
