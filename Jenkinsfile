pipeline {
    agent any
    tools {
        maven 'Maven 3.9.9' // Ensure this name matches the configured Maven tool in Jenkins
    }
    stages {
        stage('Compile Stage') {
            steps {
                bat 'mvn clean compile' // Use 'bat' instead of 'sh' for Windows
            }
        }
        stage('Testing Stage') {
            steps {
                bat 'mvn test'
            }
        }
        stage('Deployment Stage') {
            steps {
                bat 'mvn deploy'
            }
        }
    }
    post {
        success {
            echo 'Build successful!'
        }
        failure {
            echo 'Build failed.'
        }
    }
}
