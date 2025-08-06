pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/Abhii707/jenkins-node-pipeline.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t my-node-app .'
            }
        }

        stage('Run Docker Container') {
            steps {
                sh 'docker run -d -p 3000:3000 --name my-node-container my-node-app'
            }
        }

        stage('Check Running Container') {
            steps {
                sh 'docker ps'
            }
        }
    }
}
