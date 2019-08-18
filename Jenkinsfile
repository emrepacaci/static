pipeline {
    agent any
     stages {
        stage('upload to AWS') { 
            steps {
                withAWS(region: 'us-west-2', credentials: 'aws') {
                    s3Upload(file: 'index.html', bucket: 'project2statiswebsite', path: 'https://github.com/emrepacaci/static.git/index.html')
                }
            }
        }
    }
}
