pipeline {
  agent any
  stages {
    stage('Lint Html') {
      steps {
<<<<<<< HEAD
        sh 'tidy -q -e *.html'
||||||| merged common ancestors
        sh tidy -q -e *.html
=======
        sh tidy-q-e *.html
>>>>>>> afb96119ef7b47936f6b0f2ca655b382142ee4ce
      }
    }
    stage('upload to AWS') {
      steps {
        withAWS(region: 'us-west-2', credentials: 'aws') {
          s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file: 'index.html', bucket: 'project2statiswebsite')
        }

      }
    }
  }
}