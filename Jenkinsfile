pipeline {
    agent any

    stages{
        stage('deploy to S3'){
            steps{
               sh 'aws s3 cp public s3://websitebucket19 --recursive'
               sh 'aws s3api put-bucket-policy --bucket websitebucket19 --policy file://policy.json'
               sh 'aws s3 website s3://websitebucket19/ --index-document index.html --error-document error.html'
             
            }
        }
    }
    
}
