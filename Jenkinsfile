pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/nabilElhady/jenkins-test-repo2'
            }
        }

        stage('Install Dependencies') {
            steps {
                bat 'npm install'
            }
        }

        stage('Test') {
            steps {
                bat 'npm test > output.txt'
            }
        }

        stage('Archive Results') {
            steps {
                archiveArtifacts artifacts: 'output.txt', fingerprint: true
            }
        }
    }
}
