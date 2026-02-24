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

        stage('test') {
            steps {
                withSonarQubeEnv(installationName: 'SonarQube' , credentialsId: 'sonar') {
                sh '''
                mvn clean verify -DskipTests sonar:sonar   -Dsonar.projectKey=testing
                                                           -Dsonar.projectName='testing'
                '''
                }
            }
        }
    }
}
