pipeline {
    agent any
  
    stages {
        stage('Checkout') {
            steps {
                git 'git branch: 'main', url: 'https://github.com/aayushid08-wq/Project-Structure.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean install -DskipTests'
            }
        }
    }
}
