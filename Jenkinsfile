pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                sh 'git https://github.com/shanthilakshmi/Python.git'
            }
        }
        stage('Build') {
            steps {
                sh 'python3 ops.py'
            }
        }
        stage('Test') {
            steps {
                sh 'python3 -m pytest'
            }
        }
    }
}
