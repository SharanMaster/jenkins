pipeline {
    agent any
    options { 
        buildDiscarder(logRotator(numToKeepStr: '15'))
    }
    stages {
        stage ('Git Checkout') {
            steps {
                checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/SharanMaster/my-app']])
            }
        }
        stage ('pwd') {
            steps {
                sh 'pwd'
            }
        }
    }
}

