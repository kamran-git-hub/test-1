pipeline {
    // Yahan hum Jenkins ko bol rahe hain ke build ke liye 'maven' ka docker container use kare
    agent { 
        docker 'maven:3.8.4-openjdk-11' 
    }
    
    stages {
        stage('Clone Java Project') {
            steps {
                echo 'Code clone ho raha hai...'
                git url: 'https://github.com/jglick/simple-maven-project-with-tests.git', branch: 'master'
            }
        }
        stage('Build inside Docker') {
            steps {
                echo 'Docker container ke andar code build ho raha hai...'
                // Yeh command ab aapke VM par nahi, balke Docker container ke andar chalegi!
                sh 'mvn clean package -DskipTests' 
            }
        }
    }
}
