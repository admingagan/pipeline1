pipeline {
      agent any
      stages {
            stage('Init') {
                  steps {
                        timeout(time: 3, unit: 'MINUTES') {
                        echo 'Hi, Welcome to Pipeline'
                        }
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
