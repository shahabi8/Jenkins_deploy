pipeline {
    agent any
    stages {
       stage('Upload to AWS') {
             steps {
                 withAWS(region:'us-east-2',credentials:'Jenkins_local') {
                 sh 'echo "Uploading content with AWS creds"'
                     s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'D:/Job/Udacity_mentorship/Update_stack_IAM.yml', bucket:'jenkins-upload-aws')
                 }
             }
        }
    }
}
