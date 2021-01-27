pipeline {
    agent any

    tools {
        maven "MAVEN_HOME"
    }

    stages {
        stage('Build') {
            steps {
                sh "mvn clean install -DskipTests"
            }
        }
		stage('Test') {
            steps {
                sh "mvn test"
            }
        }
		stage('sonarqube') {
            steps {
                sh "mvn clean sonar:sonar"
            }
        }
    }
}
