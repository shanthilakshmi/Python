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
        stage('compile') {
            steps {
                sh 'python3 -m py_compile Samplefile.py'
            }
        }
        stage('Test') {
            steps {
                sh 'python3 -m pytest --junit-xml test_Samplefile.py'
            }
        }
        stage('Deliver'){
            steps {
            sh'python3 pyinstaller -F Samplefile.py'
            }
        }
    }
}
