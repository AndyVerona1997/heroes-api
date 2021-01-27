pipeline {
    agent any

    tools {
        maven "MAVEN_HOME"
    }

    stages {
        stage('Build') {
            steps {
                sh "mvn clean install -DskipTest=true"
            }
        }
		stage('Test') {
            steps {
                sh "mvn Test"
            }
        }
    }
}
