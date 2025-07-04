pipeline {
    agent any

    stages {
        stage('Clone') {
    steps {
        git branch: 'main', url: 'https://github.com/nabilElhady/jenkins-test-repo2'
    }
}

        stage('Install Dependencies') {
            steps {
                bat 'npm install'
            }
        }

        stage('Test') {
            steps {
                bat 'npm test'
            }
        }
    }
}
