pipeline {
    agent any
  
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/aayushid08-wq/Project-Structure.git'
            }
        }

        stage('Build') {
            steps {
                sh '''
                cd backend
                mvn clean package -DskipTests
                '''
            }
        }
    }
}
