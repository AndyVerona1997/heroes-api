pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean install -DskipTest=true'
            }
        }
        
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        
    }
}
