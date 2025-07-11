pipeline {
    agent {
        label 'slave2'
    }
    environment {
        DEPLOY_TO = 'production'
    }
    stages {
        stage('deploytodev') {
            steps {
                echo "deploy to dev"
            }
        }
        stage('deploytoprod') {
            when {
                anyOf {
                   branch 'production'
                environment name: 'DEPLOY_TO', value: 'production'  
                }
            }
            steps {
                echo "deploy to prod"
            }
        }
    }
}
