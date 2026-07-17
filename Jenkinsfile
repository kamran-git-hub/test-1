pipeline {
    agent any
    
    tools {
        // Sirf Maven rakhein, jdk hata dein
        maven 'Maven3' 
    }

    stages {
        stage('Clone Java Project') {
            steps {
                echo 'Basic Java project clone ho raha hai...'
                // Nayi aur aasan dummy repository
                git url: 'https://github.com/jglick/simple-maven-project-with-tests.git', branch: 'master'
            }
        }
        stage('Build with Maven') {
            steps {
                echo 'Maven dependencies download kar raha hai aur .jar file bana raha hai...'
                sh 'mvn clean package' 
            }
        }
    }
}
