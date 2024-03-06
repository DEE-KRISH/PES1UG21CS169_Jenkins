pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                // Compile the C++ program
                sh 'g++ -o hello hello.cpp'
                echo 'Build Stage Successful'
            }
        }
        stage('Test') {
            steps {
                // Run the compiled program
                sh './hello'
                echo 'Test Stage Successful'
                // Add post condition for test results if needed
            }
        }
        stage('Deploy') {
            steps {
                // Add deployment steps if needed
                echo 'Deploy Successful'
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
