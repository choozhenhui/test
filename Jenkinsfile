pipeline {
    agent any

    environment {
        GITHUB_USERNAME = 'choozhenhui'
        GITHUB_TOKEN = credentials('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') // Jenkins credentials ID
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
