pipeline {
    agent any
    stages {
        stage('Upload to AWS') {
            steps {
                    withAWS(region:'us-east-2', credentials:'jenkins'){
                    s3Upload(file:'index.html', bucket:'cloud-website-new2020', path:'/Jenkins-AWS/index.html')
                }  
            }
        }
    }
}