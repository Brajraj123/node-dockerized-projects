pipeline {
    agent any
    stages {
        stage("Setup") {
            steps {
                // Install nvm
                sh 'curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash'
                sh 'export NVM_DIR="$HOME/.nvm"'
                sh '[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"'
                sh '[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"'
                
                // Install Node.js and npm
                sh 'nvm install node'
                sh 'nvm use node'
            }
        }
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
