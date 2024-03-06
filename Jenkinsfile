pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                // Define build steps here
                sh 'make'
            }
        }
        stage('Test') {
            steps {
                // Define test steps here
                sh 'make test'
            }
        }
        stage('Deploy') {
            steps {
                // Define deployment steps here
                sh 'make deploy'
            }
        }
    }
    
    post {
        always {
            echo 'Pipeline completed'
        }
        failure {
            echo 'Pipeline failed'
        }
    }
}
