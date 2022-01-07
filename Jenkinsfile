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
                  steps {
                  build job: 'my-dsl-job-1'
                  }
            }
            stage('Test') {
                  steps {
                        echo "Testing being conducted"
                  }
                  steps {
                  build job: 'my-dsl-job-2'
                  }
            }
            stage('Deploy Production') {
                  steps {
                        echo "Deploying in Production Area"
                  }
            }
      }
}
