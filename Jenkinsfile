pipeline {
    agent any
    tools {
        maven 'Maven 3.9.9' // Name of the Maven tool configured in Jenkins
    }
    stages {
        stage('Compile Stage') {
            steps {
                withMaven(maven: 'Maven 3.9.9') { // Use the configured Maven name
                    sh 'mvn clean compile'
                }
            }
        }
        stage('Testing Stage') {
            steps {
                withMaven(maven: 'Maven 3.9.9') { // Use the configured Maven name
                    sh 'mvn test'
                }
            }
        }
        stage('Deployment Stage') {
            steps {
                withMaven(maven: 'Maven 3.9.9') { // Use the configured Maven name
                    sh 'mvn deploy'
                }
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
