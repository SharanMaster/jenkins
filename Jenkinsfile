pipeline {
    agent any
    options { 
        buildDiscarder(logRotator(numToKeepStr: '15'))
    }
    stages {
        stage (Changes) {
            steps {
                sh 'pwd'
            }
        }   
    }
}

