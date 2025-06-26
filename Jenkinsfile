pipeline {
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
        stage('Deploy stage') {
            steps {
                echo 'Deploying in stage environment...'
                sleep 5
                echo 'Successfully deployed in stage'
            }
        }
    }
}
