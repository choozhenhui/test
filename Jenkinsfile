pipeline {
    agent any
    tools {
        jdk 'Java17'
        maven 'Maven3'
    }
    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from the repository
                git 'https://github.com/choozhenhui/test'
            }
        }
        stage('Build with maven') {
            steps {
                // Run Maven install
               
                bat 'mvn -B clean install'
            }
        }
    }
    post {
 
        success {
            // Notify success
            echo 'Build succeeded!'
        }
        failure {
            // Notify failure
            echo 'Build failed!'
        }
       
    }
}
