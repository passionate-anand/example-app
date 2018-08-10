pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building...'
            }
        
        }
        stage('zip') {
            sh 'zip -r ${env.BUILD_TAG}.zip . '
        }
        stage('s3_upload'){
            sh 'aws w3 cp ${env.BUILd_TAG}.zip s3://'
        }
        stage('Test') {
            steps {
                echo 'Testing...'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
