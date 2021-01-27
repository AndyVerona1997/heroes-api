pipeline {
    agent any

    tools {
        maven "MAVEN_HOME"
    }

    stages {
        stage('Deploy') {
            when {
                branch 'master'
            }
            steps {
                	sh "mvn deploy"
            }
        }
	}
}
