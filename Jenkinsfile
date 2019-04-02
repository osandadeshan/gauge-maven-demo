pipeline {
    environment {
        CI = 'true'
    }
    stages {
        stage('Test') {
            steps {
                mvn test-compile gauge:execute -DspecsDir="specs/login.spec" -Denv="dev"
            }
        }
        stage('Build') {
            steps {
                mvn clean install -DskipTests
            }
        }
    }
}