pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                sh 'git clone https://github.com/shanthilakshmi/Python.git'
            }
        }
        stage('Build') {
            steps {
                sh 'python3 Samplefile.py'
            }
        }
        stage('Test') {
            steps {
                sh 'python3 -m pytest'
            }
        }
    }
}
