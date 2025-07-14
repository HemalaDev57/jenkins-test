pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Deploy to Dev') {
            steps {
                echo 'Running build step...'
                echo 'Build completed successfully!'
            }
        }
        stage('Parallel Tests') {
            parallel {
                stage('Unit Tests') {
                    steps {
                        echo 'Running unit tests...'
                    }
                }
                stage('Integration Tests') {
                    steps {
                        echo 'Running integration tests...'
                    }
                }
                stage('Static Analysis') {
                    steps {
                        echo 'Running static code analysis...'
                    }
                }
            }
        }

        stage('Nested Deploy') {
            stages {
                stage('Deploy to Dev') {
                    steps {
                        echo 'Deploying to Dev environment...'
                    }
                }
                stage('Deploy to QA') {
                    steps {
                        echo 'Deploying to QA environment...'
                    }
                }
            }
        }

        stage('Cleanup') {
            steps {
                echo 'Cleaning up workspace...'
            }
        }
    }
}
