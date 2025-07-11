pipeline {
    agent {
        label 'slave2'
    }
    stages {
        stage('expressionstage') {
            when {
                expression { BRANCH_NAME ==~ /(prod|main)/ }
            }
            steps {
                echo "this from expression condition"
            }
        }
    }
}
