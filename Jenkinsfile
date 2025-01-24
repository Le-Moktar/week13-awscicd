pipeline {
    agent any

    stages {
        stage('build'){
            steps{
                sh 'echo build'
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
    }
}