pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'docker build -t api .'
            }
        }
        stage('Push to Docker Hub') {
            steps {
                sh 'docker login -u SeppeVdb -p Azerty123'
                sh 'docker tag api SeppeVdb/api:latest'
                sh 'docker push SeppeVdb/api:latest'
            }
        }
    }
}