pipeline {
    agent any

    stages {
        stage('Clean repo') {
            steps {
                sh ' rm -rf Python '
            }
        }
        //stage('Checkout') {
           // steps {
             //   sh 'git clone https://github.com/shanthilakshmi/Python.git'
            //}
       // }
        stage('Build') {
            steps {
                sh 'python3 py_compile Samplefile.py'
            }
        }
        stage('Test') {
            steps {
                sh 'python3 -m pytest'
            }
        }
    }
}
