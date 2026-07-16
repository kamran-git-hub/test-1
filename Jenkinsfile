pipeline {
    agent any
    
    stages {
        stage('Clone/Checkout') {
            steps {
                echo 'GitHub se code clone ho raha hai...'
            }
        }
        stage('Build') {
            steps {
                echo 'Code build ho raha hai...'
                sh 'echo "Yeh ek dummy Linux build command hai"'
            }
        }
        stage('Test') {
            steps {
                echo 'Code test ho raha hai...'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Application server par deploy ho rahi hai...'
            }
        }
    }
    
    post {
        always {
            echo 'Pipeline khatam ho gayi hai. Yeh always block hai jo hamesha chalega!'
        }
        success {
            echo 'Wah! Build successful ho gaya.'
        }
    }
}
