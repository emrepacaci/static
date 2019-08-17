pipeline {
     stages {
        stage('Build') { 
            steps {
                sh 'echo "Hello World"'
                sh '''
                    scho "Multiline shells work too"
                    ls -lah
                ''' 
            }
        }
    }
}
