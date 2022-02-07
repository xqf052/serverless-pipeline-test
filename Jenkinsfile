pipeline {
    agent { 
        docker {  image 'serverlesspolska/serverless-framework:latest' }
        }

    stages {
        stage('serverless deploy') {
            steps{
                dir('./serverless-deploy'){
                    sh 'ls'
                    sh 'serverless -version'
                     withAWS(credentials: 'xqf052aws1-cred', region:'ap-southeast-2'){
                        sh 'sls deploy -v'
                    }
                }
            }
        }

    }
}