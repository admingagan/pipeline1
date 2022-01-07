
pipeline {
    agent none
    stages {
        stage('Non-Sequential Stage') {
            steps {
                echo "On Non-Sequential Stage"
            }
        }
        stage('Sequential') {
            environment {
                FOR_SEQUENTIAL = "some-value"
            }
            stages {
                stage('In Sequential 1') {
                    steps {
                        echo "In Sequential 1"
                        sleep 10
                    }
                }
                stage('In Sequential 2') {
                    steps {
                        echo "In Sequential 2"
                        sleep 10
                    }
                }
                stage('Parallel In Sequential') {
                    parallel {
                        stage('In Parallel 1') {
                            steps {
                                echo "In Parallel 1"
                                sleep 10
                            }
                        }
                        stage('In Parallel 2') {
                            steps {
                                echo "In Parallel 2"
                                sleep 10
                            }
                        }
                    }
                }
            }
        }
    }
}
