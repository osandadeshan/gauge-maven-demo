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
                'mvn test-compile gauge:execute -DspecsDir=specs'
            }
        }
        stage('Build') {
            steps {
                'mvn clean install -DskipTests'
            }
        }
    }
}