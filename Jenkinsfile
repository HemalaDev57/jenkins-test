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

        stage('Deploy and Test - Stage & QA') {
            parallel {
                stage('Stage Deploy & Test') {
                    stages {
                        stage('Deploy Stage') {
                            steps {
                                echo 'Deploying in stage environment...'
                                sleep 5
                                echo 'Successfully deployed in stage'
                            }
                        }
                        stage('Test Stage') {
                            steps {
                                echo 'Running automated test in stage...'
                                sleep 5
                                echo 'Successfully deployed and tested in stage'
                            }
                        }
                    }
                }

                stage('QA Deploy & Test') {
                    stages {
                        stage('Deploy QA') {
                            steps {
                                echo 'Deploying in QA environment...'
                                sleep 5
                                echo 'Successfully deployed in QA'
                            }
                        }
                        stage('Test QA') {
                            steps {
                                echo 'Running automated test in QA...'
                                sleep 5
                                echo 'Successfully deployed and tested in QA'
                            }
                        }
                    }
                }
            }
        }

        stage('Deploy Prod') {
            steps {
                echo 'Deploying in prod environment...'
                sleep 5
                echo 'Successfully deployed in prod'
            }
        }

        stage('Automated test - prod') {
            steps {
                echo 'Running automated test in prod...'
                sleep 5
                echo 'Successfully deployed and tested in prod'
            }
        }
    }
}
