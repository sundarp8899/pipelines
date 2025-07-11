pipeline {
    agent {
        lable 'slave2'
    }
    environment {
        TODAYS_DAY = 'thursday'
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
