pipeline {
  agent any
  stages {
    stage('Lint Html') {
      steps {
        sh 'tidy -q -e *.html'
      }
    }
    stage('upload to AWS') {
      steps {
        withAWS(region: 'us-west-2', credentials: 'aws') {
          s3Upload(file: 'index.html', bucket: 'project2statiswebsite', path: 'index.html')
        }

      }
    }
  }
}