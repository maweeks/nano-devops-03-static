pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                withAWS(region:'us-west-2', credentials:'aws-static') {
                    s3Upload(
                        pathStyleAccessEnabled: true,
                        payloadSigningEnabled: true,
                        file:'index.html',
                        bucket:'nano-devops-03'
                    )
                }
            }
        }
    }
}