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
		stage('sonarqube') {
            steps {
                sh "mvn sonar:sonar"
            }
        }
		stage('Deploy') {
            when {
                branch 'master'
            }
            steps {
                	sh "./mvnw deploy"
            }
        }
	}
}
