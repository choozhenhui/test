pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/choozhenhui/test.git'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                sh 'mvn deploy'
            }
        }
    }
}
