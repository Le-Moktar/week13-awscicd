pipeline {
    agent any

    environment{
        BRANCH_NAME = 'main'
        GIT_URL = 'https://github.com/Le-Moktar/week13-awscicd.git'
        IMAGE_TAG = 'awscicd'
        IMAGE_VERSION = '${BUILD_ID}'
    }

    stages {
        stage('git checkout'){
            steps{
                git branch: "${BRANCH_NAME}", url: "${GIT_URL}"
            }
        }
        stage('docker build'){
            steps{
                sh 'docker build -t "${IMAGE_TAG}" .'
                sh 'docker images'
            }
        }
       
    }
}