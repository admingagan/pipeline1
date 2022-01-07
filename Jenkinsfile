pipeline {
    agent any
    stages {
        stage('Build Application') {
            steps {
                sh echo "hello from build"
            }
            post {
                success {
                    echo "Now Archiving the Artifacts...."
                   }
            }
        }
        stage('Deploy in Staging Environment'){
            steps{
                build job: 'my-dsl-test-project'
             }
            
        }
        stage('Deploy to Production'){
            steps{
                timeout(time:5, unit:'DAYS'){
                    input message:'Approve PRODUCTION Deployment?'
                }
                build job: 'my-dsl-job-1'
            }
        }
    }
}
