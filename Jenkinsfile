pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Running build step...'
                echo 'Build completed successfully!'
            }
        }
    }
}
