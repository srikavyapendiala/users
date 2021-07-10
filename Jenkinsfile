pipeline{
    agent any
    stages {
        stage('prepare Artifacts') {
            steps {
                sh '''
                zip -r users.zip *
            '''
            }
        }
        stage('upload Artifacts') {
            steps {
                sh '''
                 curl -f -v -u admin:kavya --upload-file users.zip http://172.31.6.66:8081/repository/users/users.zip
            '''
            }
        }
    }
}
