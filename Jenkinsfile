pipeline {
  agent {
      label 'MaxSoft WebBot Test Suite'
  }
    environment {
        CI = 'true'
    }
    stages {
        stage('Test') {
            steps {
                bat 'mvn test-compile gauge:execute -DspecsDir=specs'
            }
        }
        stage('Build') {
            steps {
                bat 'mvn clean install -DskipTests'
            }
        }
    }
}