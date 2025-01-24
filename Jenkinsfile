pipeline {
    agent any

    stages {
        stage('git checkout'){
            steps{
                git branch: 'main', url: 'https://github.com/Le-Moktar/week13-awscicd.git'
            }
        }
        stage('test'){
            steps{
                sh 'echo test'
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