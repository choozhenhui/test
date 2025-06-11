pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                bat 'mvn clean install'
            }
        }
        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                bat 'mvn deploy -DaltDeploymentRepository=internal.repo::default::https://github.com/choozhenhui/test/maven-snapshots/'
            }
        }
    }
}
