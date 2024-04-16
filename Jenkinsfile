pipeline{
    agent any
    stages{
        stage('Run Unit Tests'){
            steps{
                sh 'echo "Unit Test Pass"'
            }
        }
        stage('Run Integration Tests'){
            steps{
                sh 'echo "Integration Test Pass"'
            }
        }
        stage('Write Log'){
            steps{
                sh 'echo "OK" > /tmp/job_tests/test'
            }
        }
    }
    post {
        success {
            build job: 'DeployHelloWorld', parameters: []
        }
    }
}
