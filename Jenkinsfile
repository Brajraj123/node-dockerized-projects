pipeline {
    agent any
    stages{
        stage("checkout"){
            steps{
                checkout scm
            }
        }

        stage("Test"){
            steps{
                sh 'sudo apt install npm'
                sh 'npu test'
            }
        }

        stage("Build"){
            steps{
                sh 'npa run build
            }
       }
    }
}
