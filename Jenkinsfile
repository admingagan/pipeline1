pipeline {
      agent any
      stages {
            stage('Init') {
                  steps {
                        echo 'Hi, Welcome to Pipeline'
                        }
            }
            stage('Build') {
                  steps {
                        echo 'Building Sample Maven Project'
                  }
            }
            stage('Test') {
                  steps {
                        echo "Testing being conducted"
                  }
            }
            stage('Deploy Production') {
                  steps {
                        echo "Deploying in Production Area"
                  }
            }
      }
}
