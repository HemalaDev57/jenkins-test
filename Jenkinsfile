pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Manual Git Checkout') {
            steps {
                sh '''
                    rm -rf myrepo
                    git clone --branch ${GIT_BRANCH} ${GIT_REPO} myrepo
                    cd myrepo
                    echo "=== Commit Info ==="
                    git log -1 --pretty=fuller
                '''
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
