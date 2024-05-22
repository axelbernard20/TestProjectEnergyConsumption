pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/axelbernard20/TestProjectEnergyConsumption.git'
            }
        }
        stage('Environment Setup') {
            steps {
                script {
                    // Set up the environment
                }
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean install'
                // 'mvn clean compile'
            }
        }
        stage('Static Analysis') {
            steps {
                sh 'mvn checkstyle:check'
            }
        }
        stage('Unit Tests') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Integration Tests') {
            steps {
                sh 'mvn verify'
            }
        }
        stage('Package') {
            steps {
                sh 'mvn package'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }
}
