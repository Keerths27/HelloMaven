pipeline {
    agent any

    tools {
        maven 'Maven 3.8.8'  // Replace with your configured Maven tool name
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
}


