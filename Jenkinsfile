pipeline {
    agent any

    tools {
        nodejs 'node18'
    }

    stages {

        stage('Clone') {
            steps {
                git 'https://github.com/bhanuprasadyadav1234-cmyk/car-website.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }

        stage('Deploy') {
            steps {
                sh 'eb deploy'
            }
        }
    }
}
