pipeline {
    agent any
  
    stages {
        stage('Checkout') {
            steps {
                git ''
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean install -DskipTests'
            }
        }
    }
}
