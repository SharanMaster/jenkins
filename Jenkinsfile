pipeline {
    agent any
    options { 
        buildDiscarder(logRotator(numToKeepStr: '15'))
    }
    stages {
        stage ('Git Checkout') {
            steps {
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/SharanMaster/jenkins']])
            }
        }
        stage ('Kubernetes Deployment') {
            steps {
                sh 'kubectl apply -f deployment.yaml'
            }
        }
    }
}

