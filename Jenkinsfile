pipeline {
    agent any
    
    tools {
        // Yeh wahi naam hona chahiye jo aapne 'Global Tool Configuration' mein rakha tha (maslan 'Maven3')
        maven 'Maven-1' 
    }

    stages {
        stage('Clone Java Project') {
            steps {
                echo 'Public Java project GitHub se clone ho raha hai...'
                // Yeh Jenkins ka official dummy Java project hai jisme pom.xml majood hai
                git url: 'https://github.com/jenkins-docs/simple-java-maven-app.git', branch: 'master'
            }
        }
        stage('Build with Maven') {
            steps {
                echo 'Maven dependencies download kar raha hai aur .jar file bana raha hai...'
                // 'mvn clean package' command purani files delete kar ke naya build banati hai
                sh 'mvn clean package' 
            }
        }
    }
}
