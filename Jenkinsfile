pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                // Compile the C++ file
                sh 'g++ -o hello hello.cpp'
            }
        }
        stage('Test') {
            steps {
                // Run the compiled program
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
