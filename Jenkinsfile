pipeline {
    agent any

    stages {
        stage('Environment Check') {
            steps {
                sh 'g++ --version'
            }
        }
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'g++ main.cpp -o my_app'
            }
        }
        stage('Test') {
            steps {
                echo 'Running Test...'
                sh './my_app'
            }
        }
    }
    post {
        success {
            echo 'Everything is perfect!'
        }
    }
}
