pipeline {
    agent any

    environment{
        BRANCH_NAME = 'main'
        GIT_URL = 'https://github.com/Le-Moktar/week13-awscicd.git'
    }

    stages {
        stage('git checkout'){
            steps{
                git branch: "${BRANCH_NAME}", url: "${GIT_URL}"
            }
        }
        stage('docker build'){
            steps{
                sh 'docker build -t week13-awscicd .'
                sh 'docker images'
            }
        }
        stage('stage number'){
            steps{
                sh 'echo stage_$BUILD_ID'
            }
        }
        // stage('System-Test'){
        //     steps{
        //         sh 'cat /etc/os-release'
        //     }
        // }
    }
}