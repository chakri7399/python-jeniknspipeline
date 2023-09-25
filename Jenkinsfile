pipeline {
    agent any

    stages {
        stage('Gitcheckout') {
            steps {
              checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/chakri7399/python-jeniknspipeline.git']])
            }
        }
        stage('Build') {
            steps {
              git branch: 'main', url: 'https://github.com/chakri7399/python-jeniknspipeline.git'
              sh 'python3 test_ops.py'
            }
        }
        stage('Test') {
            steps {
              sh 'pytest test_ops.py'
            }
        }
    }
}
