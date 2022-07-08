

@Library('veinmind-runner') _

pipeline {
    agent any

    stages {
        stage('build') {
            steps {
                script {
                    sh 'docker build -t weak:latest -f Dockerfile .'
                }
            }
        }
    }
    stage('scan') {
        steps {
            script {
                veinmindRunner.scan("weak:latest", 1)
            }
        }
    }
}