pipeline {
    agent any

    environment {
        GITHUB_USERNAME = 'choozhenhui'
        GITHUB_TOKEN = credentials('github-pat') // Jenkins credentials ID
    }

    stages {
        stage('Build') {
            steps {
                script {
                    bat 'mvn clean install'
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    bat 'mvn deploy -DaltDeploymentRepository=github::default::https://maven.pkg.github.com/choozhenhui/test'
                }
            }
        }
    }
}
