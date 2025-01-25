pipeline {
    agent any

    environment{
        BRANCH_NAME = 'main'
        GIT_URL = 'https://github.com/Le-Moktar/week13-awscicd.git'
        IMAGE_TAG = 'awscicd'
        IMAGE_VERSION = "${BUILD_NUMBER}"
    }

    stages {
        stage('git checkout'){
            steps{
                git branch: "${BRANCH_NAME}", url: "${GIT_URL}"
            }
        }
        stage('docker build'){
            steps{
                sh 'docker build -t "${IMAGE_TAG}:${IMAGE_VERSION}" .'
                sh 'docker images'
            }
        }
       stage('system check'){
            steps{
                sh 'pwd'
                sh 'ls'
                sh 'cat /etc/os-release'
            }
        }
    }
}