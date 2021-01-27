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
  stage('SonarQube analysis') {
    // requires SonarQube Scanner 2.8+
    def scannerHome = tool 'sonarScanner';//Mismo nombre que pusimos // en el global tool configuration
    withSonarQubeEnv('sonarExample') { // El nombre de servidor que //pusimos en Configuración del sistema.
      sh "${scannerHome}/bin/sonar-scanner -Dsonar.projectKey=fr.demo:my-project -Dsonar.sources=. -Dsonar.java.binaries=."
    }
  }
}
