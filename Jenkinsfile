pipeline {
    agent any

    tools {
        maven 'Maven 3.9.6'  // Ensure you configured this in Jenkins > Global Tool Configuration
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Keerths27/HelloMaven.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
    }

    post {
        success {
            echo '✅ Build succeeded. Archiving artifacts...'
            archiveArtifacts artifacts: 'target/*.jar', fingerprint: true
        }
        failure {
            echo '❌ Build failed. Please check logs.'
        }
    }
}

