pipeline {
    agent { 
        docker {  image 'yfy668/serverless:v1.0.2' }
        }

    stages {
        stage('serverless deploy') {
            steps{
                dir('/var/jenkins_home/workspace/serverless-pipeline-test/serverless-deploy'){
                     withAWS(credentials: 'xqf052aws1-cred', region:'ap-southeast-2'){
                        sh 'sls deploy -v'
                    }
                }
            }
        }

    }
}