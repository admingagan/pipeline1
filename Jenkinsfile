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
                  build job: 'my-dsl-job-1'
                  }
            }
            stage('Test') {
                  steps {
                  build job: 'my-dsl-job-2'
                  }
            }
            stage('Deploy Production') {
                  steps {
                    timeout(time:5, unit:'DAYS'){
                    input message:'Approve PRODUCTION Deployment?'
                    }
                        echo "Deploying in Production Area"
                  }
            }
      }
}
