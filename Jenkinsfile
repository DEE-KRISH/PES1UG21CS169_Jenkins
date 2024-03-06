pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o hello hello.cpp'
            }
        }
        stage('Test') {
            steps {
                sh './hello'
            }
        }
        stage('Deploy') {
            steps {
                // Add deployment steps if needed
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
