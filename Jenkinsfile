pipeline{
        agent any
        stages {
            stage('Upload to AWS') {
                steps {
                    retry(3){
                        withAWS(region:'us-east-2', credentials:'jenkins'){
                        s3Upload(file:'*.*', bucket:'cloud-website-new2020', path:'Jenkins-AWS/')
                        }
                    }                             
                }
            }
        }
}