pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Keerths27/HelloMaven.git'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean package'   // Builds your project
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'           // Runs tests
            }
        }
    }
}


