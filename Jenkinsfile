pipeline {
    agent { 
        docker {  image 'yfy668/serverless:v1.0.2' }
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