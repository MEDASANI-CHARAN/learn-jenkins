pipeline {
    agent {
        label 'agent-1'
    }
    options {
                timeout(time: 60, unit: 'SECONDS')
                disableConcurrentBuilds()
            }
    stages {
        stage('Build') {
            steps {
                sh 'echo this is build'
            }
        }
        stage('Test') {
            steps {
                sh 'echo this is test'
                sh 'sleep 10'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo this is deploy'
            }
        }
    }
}