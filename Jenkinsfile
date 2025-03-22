pipeline {
    agent any

    environment {
        GITHUB_REPO = 'https://github.com/your-username/your-repo.git'
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                sh 'echo Building the project...'
                // Example: sh './gradlew build' or 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                sh 'echo Running tests...'
                // Example: sh './gradlew test' or 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                sh 'echo Deploying application...'
                // Example: sh './deploy.sh'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed! Check logs for details.'
        }
    }
}
