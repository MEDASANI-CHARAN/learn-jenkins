pipeline {
    agent {
        label 'var'
    }
    options {
                timeout(time: 60, unit: 'SECONDS')
                disableConcurrentBuilds() 
            }
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }
     environment {
        DEPLOY_TO = 'production' 
        GREETING = 'Good Morning'
        }
    stages {
        stage('Build') {
            steps {
                sh 'echo this is build'
                sh 'env'
            }
        }
        stage('Test') {
            steps {
                sh 'echo this is test'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo this is deploy'
            }
        }
        stage('print params') {
            steps {
                echo "Hello ${params.PERSON}"

                echo "Biography: ${params.BIOGRAPHY}"

                echo "Toggle: ${params.TOGGLE}"

                echo "Choice: ${params.CHOICE}"

                echo "Password: ${params.PASSWORD}"

                echo "triggred again"
            } 
        }
    }
    post { 
            always { 
                echo 'I will always say Hello again!'
            }
         }
}