pipeline {
    agent {
        label 'slave2'
    }
    environment {
        TODAYS_DAY = 'wedneday'
    }
    stages {
        stage('bulidstage') {
            when {
                environment name: 'TODAYS_DAY', value: 'thursday'
            }
            steps {
                echo "pipeline for when stage"
            }
        }
    }
}
