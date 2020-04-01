pipeline{
        agent any
        stages {
            stage('Upload to AWS') {
                steps {
                    retry(3){
                        withAWS(region:'us-east-2', credentials:'AKIA2YFUV2EBEY2HFYH3kge6mfu6guZrYyYnqd9EzTTYTlv+/kHPI4O2izah'){
                        s3Upload(file:'index.html', bucket:'cloud-website-new2020', path:'')
                        }
                    }                             
                }
            }
        }
}