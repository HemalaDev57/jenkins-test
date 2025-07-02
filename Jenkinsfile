pipeline {
    triggers {
        cron('1 * * * *') // Runs every 5 minutes
    }
    agent any
    stages {
        stage('Checkout') {
            steps {
                echo 'Checkout the current repo'
                sleep 3
            }
        }
        stage('Build') {
            steps {
                echo 'Running build...'
                sleep 5
                echo 'Build successful'
            }
        }
        stage('Test') {
            steps {
                echo 'Running test...'
                sleep 5
                echo 'Test successful'
            }
        }
    }
}
